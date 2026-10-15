# External Systems & Cores

Starting with RePlayOS 2.1.0, you can add a compatible libretro core as its own system. It appears in the normal system browser and lists supported files from its ROM folder.

## Install a core

Obtain a Linux ARM64 libretro build compatible with your Raspberry Pi and the libraries installed in RePlayOS. The `devices` setting describes compatibility; it does not make a Pi 5-only build work on Pi 3 or Pi 4.

Place the library and its matching configuration directly in `/opt/replay/cores/`. Do not create a subfolder. Example:

```text
/opt/replay/cores/
    retrotv_libretro.so
    retrotv_libretro.cfg
```

Both filenames must have the same stem and end in `_libretro.so` and `_libretro.cfg`. RePlay derives the library path from the configuration filename.

Create `retrotv_libretro.cfg` as a plain-text file:

```ini
id = "retrotv"
name = "RetroTV"
extensions = "m3u|m3u8|txt"
devices = "pi5"
```

This example declares Pi 5 support for RetroTV. For a core that supports all three models, use:

```ini
devices = "pi3|pi4|pi5"
```

All four fields are required:

| Field | Meaning |
| --- | --- |
| `id` | Unique system key and ROM folder name. Use up to 63 lowercase ASCII letters, digits or underscores, starting with a letter. Keep it unchanged to retain the system's settings and references. |
| `name` | Displayed system name, up to 127 UTF-8 bytes. |
| `extensions` | Supported file extensions in lowercase, without dots, separated by `\|`. |
| `devices` | Supported models: `pi3`, `pi4`, `pi5`, separated by `\|`. |

Use double quotes as shown. Blank lines and comments starting with `#` or `;` are allowed. Unknown or repeated fields, section headers, and empty list elements are rejected.

Use [SSH or SFTP](terminal.md) to copy the files. Stop RePlay before replacing a core that may be loaded:

```sh
# On RePlayOS over SSH:
systemctl stop replay.service
```

```sh
# On your computer, from the directory containing the two files:
scp retrotv_libretro.so retrotv_libretro.cfg root@replay.local:/opt/replay/cores/
```

```sh
# On RePlayOS over SSH:
systemctl start replay.service
```

Registrations are read at frontend startup. Restart RePlay after adding, editing, or removing a pair.

## Add content

RePlay creates `roms/<id>/` on the selected ROM storage when preparing its folders. With the example above:

```text
roms/retrotv/
    Home TV.txt
    Cartoons.m3u
```

You can create the folder yourself before restarting. Copy files in formats supported by the core and listed in `extensions`.

**Visibility > Show external systems**, controls their appearance in the main system list. It is **On** by default.

## Settings, saves, and remote launching

External cores use the existing System Settings and RePlay options, including system, folder, and game overrides. Saves, captures, and input profiles use the usual system key and configured storage/data location. RePlay ensures the save directory exists before exposing it to the core. Features such as save states depend on what the core implements.

Favorites, Recents, and [autostart](autostart.md) work as usual. Keep `id` and content paths stable so those references remain valid.

The existing [REST API](rest_api.md) accepts the configured ID as `system`:

```text
/api/v1/load_game?system=retrotv&game_file=Home%20TV.txt
```

`game_file` is relative to `roms/retrotv/`. Existing API authentication and path restrictions still apply. External playlist files are passed intact to the core, including single-entry M3Us.

## Updates and removal

Normal OTA updates update packaged official files and preserve additional, unowned files in the cores directory, provided a package does not introduce the same filenames. No reinstall is needed merely because an OTA update ran. Reflashing or replacing the operating-system partition is different; keep a backup of your external pair.

Preserving files does not guarantee binary compatibility after an OS library update. If a dependency changes, obtain a compatible build from the core's maintainer.

To unregister a system, stop RePlay, remove only that external core's `.so` and `.cfg`, and start RePlay again. ROMs, saves, and settings are retained.

## Troubleshooting

For detailed logs, set **System > Log level** to **Warn** (or a more verbose level), then restart RePlay or retry the launch. Logging may otherwise be disabled. See [Debug Information](loginfo.md).

| Symptom | Check |
| --- | --- |
| System does not appear | Restart RePlay, enable **Show external systems**, check the selected ROM storage and supported device, and add content if **Hide empty folders** is enabled. |
| Registration rejected | Check the four fields, filename pairing, and `/var/log/replay.log`. Both files must be regular files, not symbolic links. |
| Duplicate ID | Give each external system a unique ID. All valid registrations sharing an ID are disabled. |
| Official ID or library rejected | Choose a new system ID and a genuinely separate core filename. External configurations cannot replace official systems, pair with official libraries, or change `cores.cfg`. |
| Core cannot load | Check the log for a missing dependency, incompatible binary, or missing libretro entry point. |
| File fails to open | Check its path, extension, contents, and the core's own configuration or network requirements. |

The frontend reports registration and loading failures and retains the menu when loading fails. External cores execute inside the frontend process, so a crash inside a core can still terminate RePlay.
