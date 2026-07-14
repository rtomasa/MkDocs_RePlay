# Custom UI Skins

RePlayOS discovers custom UI skins from the `skins` folder on the active storage unit. The folder is created automatically for SD, USB, NVMe and NFS storage.

For example, when USB storage is selected, custom skins are loaded from:

```text
/media/usb/skins
```

## Installing a skin

Create or copy one self-contained folder for each skin:

```text
skins/
└── midnight-arcade/
    ├── skin.json
    ├── menu.png
    ├── selector.png
    ├── info.png
    └── systems/
        └── nintendo_snes/
            ├── menu.png
            ├── selector.png
            └── info.png
```

The folder name is the stable skin ID. It may contain letters, numbers, hyphens and underscores. After copying the folder, select the skin from **RePlay Options > System > Skin**.

## Manifest

Every skin requires a `skin.json` file whose `id` exactly matches its folder name:

```json
{
  "id": "midnight-arcade",
  "name": "Midnight Arcade",
  "author": "Example Author",
  "version": 1
}
```

`name` is the label displayed in the RePlayOS skin selector.

## Image requirements

| File | Dimensions | Purpose |
| --- | ---: | --- |
| `menu.png` | 192 × 192 | Main UI background |
| `selector.png` | 192 × 9 | Selected-row graphic |
| `info.png` | 192 × 16 | Information panel background |

Images must be PNG files. Missing base components fall back to the bundled RePlay skin. Images with incorrect dimensions are ignored.

## Per-system skins

Per-system images are available to all users. Put overrides under `systems/<system-key>/`, using the same internal system keys as the ROM folders, such as `nintendo_snes`, `arcade_fbneo` or `sony_psx`.

Each component is optional and falls back independently to the selected base skin. For example, a system folder containing only `selector.png` changes the selector while retaining the base `menu.png` and `info.png`.

Special folders such as favorites, recents and the media player do not load per-system overrides.

## Configuration

The selected folder ID is stored in `/media/sd/config/replay.cfg`:

```cfg
system_skin = "midnight-arcade"
```

If the configured skin is missing or invalid, RePlayOS selects the bundled `replay` skin. The previous numeric skin-slot format is no longer supported.
