# RePlay REST API

RePlay includes a small HTTP JSON API for local or LAN control. It is plain HTTP only, not HTTPS.

The server listens on port `55356` when the `system_net_control` system option is enabled.

Base URL:

```text
http://<replay-ip>:55356/api/v1
```

All endpoints use `GET` and return `application/json`. Query string values should be URL encoded. Spaces may be encoded as `%20` or `+`.

## Authentication

All API requests except `get_version` must include the net control code in the `X-RePlay-Token` HTTP header. The code is shown in `SYSTEM > INFORMATION > NET CONTROL CODE`.

Example:

```bash
curl -H 'X-RePlay-Token: 123456' 'http://<replay-ip>:55356/api/v1/get_status'
```

Missing or invalid tokens return `401 Unauthorized`. Repeated invalid attempts may temporarily return `429 Too Many Requests`.

## Errors

Common error responses:

```json
{"error":"Bad Request"}
```

Some validation errors include a detail field:

```json
{"error":"Invalid Command","detail":"Allowed commands: ..."}
```

Unsupported methods return `405 Method Not Allowed`. Unknown endpoints return `404 Not Found`.

## Get Version

Returns the RePlayOS version.

This endpoint does not require authentication, allowing clients to discover the RePlayOS version before authenticating.

```text
GET /api/v1/get_version
```

Example:

```bash
curl 'http://<replay-ip>:55356/api/v1/get_version'
```

Response:

```json
{
  "version": "RePlayOS v1.7.3"
}
```

## Get Status

Returns current system, game, UI view, pause, halt, and core information.

The `paused` field reports whether core execution is paused. The `halted` field independently reports whether the frontend has been halted using `set_cmd?cmd=halt`. Both fields may be `true` at the same time.

```text
GET /api/v1/get_status
```

Example:

```bash
curl -H 'X-RePlay-Token: 123456' 'http://<replay-ip>:55356/api/v1/get_status'
```

Response:

```json
{
  "system": "arcade_fbneo",
  "game_file": "/media/nvme/roms/arcade_fbneo/altbeast.zip",
  "game_name": "Altered Beast (set 8) (8751 317-0078)",
  "paused": false,
  "halted": false,
  "view": "game_play",
  "view_id": 2,
  "core_file": "fbneo_libretro.so",
  "core_info": "FinalBurn Neo v1.0.0.03"
}
```

Known `view` values:

| `view_id` | `view` |
| --- | --- |
| `0` | `system_list` |
| `1` | `system_options` |
| `2` | `game_play` |
| `3` | `game_options` |
| `4` | `achievements` |
| `5` | `leaderboards` |

## Get Info

Returns system hardware, resource, display, and active core/game resolution information.

```text
GET /api/v1/get_info
```

Example:

```bash
curl -H 'X-RePlay-Token: 123456' 'http://<replay-ip>:55356/api/v1/get_info'
```

Response:

```json
{
  "version": "RePlayOS v1.7.4",
  "model": "Raspberry Pi 5",
  "eeprom": "2025-11-05",
  "cpu_frequency_mhz": 2400,
  "gpu_frequency_mhz": 800,
  "cpu_temperature_c": 48.2,
  "available_ram_mb": 8192,
  "available_space_bytes": 123456789,
  "display": "DISPLAY NAME, VEN",
  "display_resolution": {
    "width": 1920,
    "height": 1080,
    "refresh_hz": 60.00
  },
  "game_resolution": {
    "width": 320,
    "height": 240,
    "refresh_hz": 59.94
  }
}
```

Fields:

| Field | Description |
| --- | --- |
| `version` | Full RePlayOS version string. |
| `model` | Detected Raspberry Pi or PC model. |
| `eeprom` | Raspberry Pi bootloader EEPROM date. It is an empty string on platforms where this information is unavailable. |
| `cpu_frequency_mhz` | Detected CPU frequency in MHz. |
| `gpu_frequency_mhz` | Detected GPU frequency in MHz. It is `0` when unavailable. |
| `cpu_temperature_c` | Current CPU temperature in degrees Celsius. It is `0.0` when unavailable. |
| `available_ram_mb` | RAM value shown in `SYSTEM > INFORMATION`, in MB. |
| `available_space_bytes` | Free space on the configured RePlay media storage, in bytes. It is `0` when unavailable. |
| `display` | Detected display name and vendor. |
| `display_resolution` | Current display width, height, and refresh rate. |
| `game_resolution` | Geometry and content refresh rate reported by the active libretro core. |

`game_resolution` is populated for any active core that reports valid geometry, including the RePlay boot menu core. It is `null` while no valid core geometry is available, such as during unload or failed-load transitions.

## Get Config

Returns the selected configuration.

```text
GET /api/v1/get_config?type=<replay|core|game>
```

The `type` parameter is mandatory:

| Type | Configuration |
| --- | --- |
| `replay` | Returns the global `replay.cfg` configuration. Sensitive fields including `nfs_*` and `wifi_*` are omitted. |
| `core` | Returns only the managed RePlay-owned options from the override file for the active game's system and display type. |
| `game` | Returns only the managed RePlay-owned options from the active game's override file. |

Example:

```bash
curl -H 'X-RePlay-Token: 123456' 'http://<replay-ip>:55356/api/v1/get_config?type=core'
```

When the selected core or game override file does not exist, the request succeeds and reports that no override is configured:

```json
{
  "type": "core",
  "configured": false,
  "config": {}
}
```

## Set Config

Updates one or more settings for the selected configuration type. The complete request is validated before any changes are written.

```text
GET /api/v1/set_config?type=<replay|core|game>&option=<option>&value=<value>
GET /api/v1/set_config?type=<replay|core|game>&option=<option-1>&value=<value-1>&option=<option-2>&value=<value-2>
```

Parameters:

| Name | Required | Description |
| --- | --- | --- |
| `type` | Yes | Configuration type: `replay`, `core`, or `game`. |
| `option` | Yes | Configuration option name. Repeat together with `value` to update multiple options. |
| `value` | Yes | New value for the corresponding `option`. |

Up to 64 changes may be included in one request. If any option or value is invalid, none of the changes are written.

### RePlay Config

It updates direct-edit `replay.cfg` options and writes all changes atomically.

Accepted RePlay options:

| Option | Values |
| --- | --- |
| `timezone_srv` | Free-form string/URL. |
| `nfs_server` | Free-form string. |
| `nfs_share` | Free-form string. |
| `nfs_version` | `3`, `4` |
| `wifi_name` | Free-form string. |
| `wifi_pwd` | Free-form string. |
| `wifi_country` | Free-form string. |
| `wifi_mode` | `wpa2`, `wpa3`, `transition` |
| `wifi_hidden` | `true`, `false` |
| `replay_insider_token` | Free-form string. |
| `replay_http_token` | Six numeric digits. |
| `rcheevos_username` | Free-form string. |
| `rcheevos_password` | Free-form string. |
| `system_kiosk_mode` | `true`, `false` |

Example:

```bash
curl -H 'X-RePlay-Token: 123456' 'http://<replay-ip>:55356/api/v1/set_config?type=replay&option=nfs_version&value=4'
```

### Core And Game Config

Core and game configuration is restricted to the common RePlay-owned options listed below. Libretro core-specific options are never returned or managed by this API.

Core and game values also accept `default`, which inherits the global RePlay value. If the selected override file does not exist, it is created containing only these managed options. Existing override files retain all unrelated core-specific options. After a successful update, the active game immediately reloads the effective game-over-core settings and an open game settings menu is refreshed.

| Option | RePlay values |
| --- | --- |
| `replay_video_ambiscan` | `0`, `1`, `2`, `3` |
| `replay_video_integer_scale` | `0`, `1`, `2`, `3`, `4`, `5` |
| `replay_video_filter` | `0` through `4` |
| `replay_video_gamma` | `0.5` through `1.5` in increments of `0.1` |
| `replay_video_monitor_x` | `-64` through `64` in increments of `4` |
| `replay_video_monitor_y` | `-64` through `64` in increments of `4` |
| `replay_audio_system_volume` | `0` through `10` |

Core and game configurations accept the same values plus `default`.

Example:

```bash
curl -H 'X-RePlay-Token: 123456' 'http://<replay-ip>:55356/api/v1/set_config?type=game&option=replay_video_filter&value=3'
```

Response:

```json
{
  "command": "set_config",
  "type": "game",
  "options": ["replay_video_filter"],
  "created": true,
  "updated": true
}
```

If no active core or game target exists, the endpoint returns `409 Configuration Unavailable`.

## Set Message

Displays a popup message in RePlay.

```text
GET /api/v1/set_msg?text=<text>&duration=<seconds>
```

Parameters:

| Name | Required | Description |
| --- | --- | --- |
| `text` | Yes | Message text. It is limited to the same maximum size as internal RePlay messages. |
| `duration` | Yes | Duration in seconds. Values `<= 0` become `1`; values `> 10` become `10`. |

Example:

```bash
curl -H 'X-RePlay-Token: 123456' 'http://<replay-ip>:55356/api/v1/set_msg?text=Hello%20world&duration=3'
```

Response:

```json
{
  "text": "Hello world",
  "duration": 3
}
```

## Save State

Queues a save-state request.

```text
GET /api/v1/save_state?slot=<slot>
```

Parameters:

| Name | Required | Description |
| --- | --- | --- |
| `slot` | Yes | Numeric save slot, from `1` to `18`. Only numbers are accepted. |

Example:

```bash
curl -H 'X-RePlay-Token: 123456' 'http://<replay-ip>:55356/api/v1/save_state?slot=1'
```

Response:

```json
{
  "command": "save_state",
  "slot": 1
}
```

Invalid slots return:

```json
{"error":"Invalid Slot"}
```

## Load State

Queues a load-state request.

```text
GET /api/v1/load_state?slot=<slot>
```

Parameters:

| Name | Required | Description |
| --- | --- | --- |
| `slot` | Yes | Numeric save slot, from `1` to `18`. Only numbers are accepted. |

Example:

```bash
curl -H 'X-RePlay-Token: 123456' 'http://<replay-ip>:55356/api/v1/load_state?slot=1'
```

Response:

```json
{
  "command": "load_state",
  "slot": 1
}
```

## Load Game

Queues a game load request.

```text
GET /api/v1/load_game?system=<system>&game_file=<relative-rom-path>
```

Parameters:

| Name | Required | Description |
| --- | --- | --- |
| `system` | Yes | System folder/name, such as `snes`. Must match a known RePlay system. |
| `game_file` | Yes | Game path relative to the system ROM folder. Absolute paths and `..` path traversal are rejected. |

Example:

```bash
curl -H 'X-RePlay-Token: 123456' 'http://<replay-ip>:55356/api/v1/load_game?system=snes&game_file=Super%20Pang%20(Japan).sfc'
```

Response:

```json
{
  "command": "load_game",
  "system": "snes",
  "game_file": "Super Pang (Japan).sfc"
}
```

Validation checks:

- `system` must exist in RePlay's system list.
- `game_file` must be relative to the selected system directory.
- The file must exist.
- The final resolved path must remain inside the system directory.
- The extension must be valid for that system.

## Set Command

Queues a general RePlay command.

```text
GET /api/v1/set_cmd?cmd=<command>
```

Supported commands:

| Command | Description |
| --- | --- |
| `reboot` | Reboot the system. |
| `power_off` | Power off the system. |
| `game_reset` | Soft reset the running core/game. |
| `game_restart` | Restart the last loaded game. |
| `screenshot` | Take a user screenshot. |
| `halt` | Toggle RePlay system halt mode. |
| `volume_up` | Increase system volume one step. |
| `volume_down` | Decrease system volume one step. |
| `mute` | Toggle mute. |

Example:

```bash
curl -H 'X-RePlay-Token: 123456' 'http://<replay-ip>:55356/api/v1/set_cmd?cmd=volume_up'
```

Response:

```json
{
  "command": "volume_up"
}
```

## Get Media Status

Returns system media information for cores that expose libretro disk control.

```text
GET /api/v1/get_media_status
```

Example:

```bash
curl -H 'X-RePlay-Token: 123456' 'http://<replay-ip>:55356/api/v1/get_media_status'
```

Response when media control is available:

```json
{
  "available": true,
  "tray_open": false,
  "current_index": 0,
  "current_number": 1,
  "count": 2,
  "images": [
    {
      "index": 0,
      "number": 1,
      "label": "Disc 1"
    },
    {
      "index": 1,
      "number": 2,
      "label": "Disc 2"
    }
  ]
}
```

Response when media control is unavailable:

```json
{
  "available": false,
  "tray_open": false,
  "current_index": 0,
  "current_number": 0,
  "count": 0,
  "images": []
}
```

`index` is zero-based and matches the libretro/RePlay internal media index. `number` is one-based and intended for display.

## Set Media

Controls system media such as CD-ROMs and floppy disks for cores that expose libretro disk control.

```text
GET /api/v1/set_media?cmd=<command>
```

Supported commands:

| Command | Extra Parameters | Description |
| --- | --- | --- |
| `open_tray` | None | Open the virtual media drive. |
| `close_tray` | None | Close the virtual media drive. |
| `next` | None | Switch to the next media image. Does not wrap around. |
| `previous` | None | Switch to the previous media image. Does not wrap around. |
| `set_index` | `index=<zero-based-index>` | Switch to a specific media image. |

Examples:

```bash
curl -H 'X-RePlay-Token: 123456' 'http://<replay-ip>:55356/api/v1/set_media?cmd=open_tray'
curl -H 'X-RePlay-Token: 123456' 'http://<replay-ip>:55356/api/v1/set_media?cmd=set_index&index=1'
curl -H 'X-RePlay-Token: 123456' 'http://<replay-ip>:55356/api/v1/set_media?cmd=next'
```

Response:

```json
{
  "command": "set_media",
  "media_command": "set_index",
  "index": 1
}
```

For `open_tray` and `close_tray`, the response omits `index`:

```json
{
  "command": "set_media",
  "media_command": "open_tray"
}
```

Boundary behavior:

- `next` at the last media image returns `409 Media Boundary`.
- `previous` at the first media image returns `409 Media Boundary`.
- There is no wraparound.

If the current core does not expose disk control, `set_media` returns `409 Media Unavailable`.
