# RePlay REST API

RePlay includes a small HTTP JSON API for local or LAN control. It is plain HTTP only, not HTTPS.

The server listens on port `55356` when the `system_net_control` system option is enabled.

Base URL:

```text
http://<replay-ip>:55356/api/v1
```

All endpoints use `GET` and return `application/json`. Query string values should be URL encoded. Spaces may be encoded as `%20` or `+`.

## Authentication

All API requests must include the net control code in the `X-RePlay-Token` HTTP header. The code is shown in `SYSTEM > INFORMATION > NET CONTROL CODE`.

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

```text
GET /api/v1/get_version
```

Example:

```bash
curl -H 'X-RePlay-Token: 123456' 'http://<replay-ip>:55356/api/v1/get_version'
```

Response:

```json
{
  "version": "RePlayOS v1.7.3"
}
```

## Get Status

Returns current system, game, UI view, pause, and core information.

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

## Get RePlay Config

Returns the current system configuration as JSON.

```text
GET /api/v1/get_replay_config
```

Example:

```bash
curl -H 'X-RePlay-Token: 123456' 'http://<replay-ip>:55356/api/v1/get_replay_config'
```

Sensitive or noisy fields are intentionally omitted from this response, including `nfs_*`, `wifi_*`.

## Set RePlay Config

Updates one direct-only `replay.cfg` configuration variable. The value is validated against the system option definition, then saved to `replay.cfg`.

```text
GET /api/v1/set_replay_config?option=<option>&value=<value>
```

Parameters:

| Name | Required | Description |
| --- | --- | --- |
| `option` | Yes | Configuration variable name. Only the variables listed below are accepted. |
| `value` | Yes | New value. It must be URL encoded and must not contain quotes or control characters. |

Accepted `option` values:

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
curl -H 'X-RePlay-Token: 123456' 'http://<replay-ip>:55356/api/v1/set_replay_config?option=nfs_version&value=4'
```

Response:

```json
{
  "command": "set_replay_config",
  "option": "nfs_version",
  "updated": true
}
```

Invalid options return the full accepted option list:

```json
{
  "error": "Invalid Option",
  "allowed_config_variables": [
    "timezone_srv",
    "nfs_server",
    "nfs_share",
    "nfs_version",
    "wifi_name",
    "wifi_pwd",
    "wifi_country",
    "wifi_mode",
    "wifi_hidden",
    "replay_insider_token",
    "replay_http_token",
    "rcheevos_username",
    "rcheevos_password",
    "system_kiosk_mode"
  ]
}
```

Invalid values return the accepted values for that option when the option has a fixed value list:

```json
{
  "error": "Invalid Value",
  "option": "wifi_mode",
  "allowed_values": ["wpa2", "wpa3", "transition"]
}
```

For free-form options, `allowed_values` is an empty array.

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
