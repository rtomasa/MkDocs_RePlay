# Folder Structure

## Root storage folders
RePlayOS utilizes a well-defined folder structure for MicroSD, USB, and NFS units. The root path, shown below, is where these directories can be found. This structure is also automatically displayed when accessing the system via SFTP:

```sh
media
├── sd
├── usb
├── nvme
└── nfs
```

## Child data folders

RePlayOS creates the following folders on the selected storage unit. When DATA LOCATION is LOCAL SD, ROMs and BIOS remain on the selected unit while config, captures, saves, skins, and Insider replays are stored on the SD card. System folders depend on the Pi model and Insider access:

```sh
storage
├── bios
├── captures
│   ├── alpha_player
│   ├── amstrad_cpc
│   ├── arcade_dc
│   ├── arcade_fbneo
│   ├── arcade_mame
│   ├── arcade_mame_2k3p
│   ├── arcade_stv
│   ├── arcade_triforce
│   ├── atari_2600
│   ├── atari_5200
│   ├── atari_7800
│   ├── atari_jaguar
│   ├── atari_jaguarcd
│   ├── atari_lynx
│   ├── commodore_ami
│   ├── commodore_amicd
│   ├── commodore_c64
│   ├── _extra
│   ├── _favorites
│   ├── ibm_pc
│   ├── microsoft_msx
│   ├── nec_pce
│   ├── nec_pcecd
│   ├── nintendo_ds
│   ├── nintendo_gb
│   ├── nintendo_gba
│   ├── nintendo_gbc
│   ├── nintendo_n64
│   ├── nintendo_gc
│   ├── nintendo_wii
│   ├── nintendo_vb
│   ├── nintendo_nes
│   ├── nintendo_snes
│   ├── panasonic_3do
│   ├── philips_cdi
│   ├── _recent
│   ├── scummvm
│   ├── sega_32x
│   ├── sega_cd
│   ├── sega_dc
│   ├── sega_gg
│   ├── sega_sg
│   ├── sega_smd
│   ├── sega_sms
│   ├── sega_st
│   ├── sharp_x68k
│   ├── sinclair_zx
│   ├── snk_ng
│   ├── snk_ngcd
│   ├── snk_ngp
│   ├── sony_psx
│   ├── sony_ps2
│   └── sony_psp
├── config
│   ├── input
│   │   ├── folder
│   │   │   ├── crt
│   │   │   └── lcd
│   │   ├── game
│   │   │   ├── crt
│   │   │   └── lcd
│   │   ├── system
│   │   │   ├── crt
│   │   │   └── lcd
│   │   ├── player_assignments.cfg
│   │   └── usercontrollerdb.txt
│   └── settings
│       ├── folder
│       │   ├── crt
│       │   └── lcd
│       ├── game
│       │   ├── crt
│       │   └── lcd
│       └── system
│           ├── crt
│           └── lcd
├── roms
│   ├── alpha_player
│   ├── amstrad_cpc
│   ├── arcade_dc
│   ├── arcade_fbneo
│   ├── arcade_mame
│   ├── arcade_mame_2k3p
│   ├── arcade_stv
│   ├── arcade_triforce
│   ├── atari_2600
│   ├── atari_5200
│   ├── atari_7800
│   ├── atari_jaguar
│   ├── atari_jaguarcd
│   ├── atari_lynx
│   ├── commodore_ami
│   ├── commodore_amicd
│   ├── commodore_c64
│   ├── _autostart
│   ├── _extra
│   ├── _favorites
│   ├── ibm_pc
│   ├── microsoft_msx
│   ├── nec_pce
│   ├── nec_pcecd
│   ├── nintendo_ds
│   ├── nintendo_gb
│   ├── nintendo_gba
│   ├── nintendo_gbc
│   ├── nintendo_n64
│   ├── nintendo_gc
│   ├── nintendo_wii
│   ├── nintendo_vb
│   ├── nintendo_nes
│   ├── nintendo_snes
│   ├── panasonic_3do
│   ├── philips_cdi
│   ├── _recent
│   ├── scummvm
│   ├── sega_32x
│   ├── sega_cd
│   ├── sega_dc
│   ├── sega_gg
│   ├── sega_sg
│   ├── sega_smd
│   ├── sega_sms
│   ├── sega_st
│   ├── sharp_x68k
│   ├── sinclair_zx
│   ├── snk_ng
│   ├── snk_ngcd
│   ├── snk_ngp
│   ├── sony_psx
│   ├── sony_ps2
│   └── sony_psp
├── replays
├── skins
└── saves
    ├── alpha_player
    ├── amstrad_cpc
    ├── arcade_dc
    ├── arcade_fbneo
    ├── arcade_mame
    ├── arcade_mame_2k3p
    ├── arcade_stv
    ├── arcade_triforce
    ├── atari_2600
    ├── atari_5200
    ├── atari_7800
    ├── atari_jaguar
    ├── atari_jaguarcd
    ├── atari_lynx
    ├── commodore_ami
    ├── commodore_amicd
    ├── commodore_c64
    ├── _extra
    ├── _favorites
    ├── ibm_pc
    ├── microsoft_msx
    ├── nec_pce
    ├── nec_pcecd
    ├── nintendo_ds
    ├── nintendo_gb
    ├── nintendo_gba
    ├── nintendo_gbc
    ├── nintendo_n64
    ├── nintendo_gc
    ├── nintendo_wii
    ├── nintendo_vb
    ├── nintendo_nes
    ├── nintendo_snes
    ├── panasonic_3do
    ├── philips_cdi
    ├── _recent
    ├── scummvm
    ├── sega_32x
    ├── sega_cd
    ├── sega_dc
    ├── sega_gg
    ├── sega_sg
    ├── sega_smd
    ├── sega_sms
    ├── sega_st
    ├── sharp_x68k
    ├── sinclair_zx
    ├── snk_ng
    ├── snk_ngcd
    ├── snk_ngp
    ├── sony_psx
    ├── sony_ps2
    └── sony_psp
```

## bios folder
It is where all system BIOS, arcade samples, sound fonts, computer special core configurations, and any other special system file are stored.

## captures folder
This is the place where screenshots are stored.

## config folder
This is where input and core configurations are saved. Input profiles can apply to a system, ROM folder, or individual game and are separated for LCD and CRT displays. Persistent Player assignments and custom physical SDL controller mappings are also stored under `config/input`.

## roms folder
This is where you can copy your game files. The system folders are prefixed by the company name for better categorization. Additionally, there are special system folders prefixed with an underscore, such as [`_autostart`](autostart.md), `_extra`, `_favorites`, and `_recent`.

## replays folder

Authenticated Insiders have a `replays/<system>/` folder containing `.rplm` input recordings. RePlay stores it at the selected data location. See [Insider Replays](replays.md) for recording and playback.

## skins folder
It contains user-installed UI skin folders. RePlayOS creates this folder automatically on the active SD, USB, NVMe or NFS unit. See [Custom UI Skins](skins.md) for the package layout and per-system overrides.

## saves folder
This folder contains all user save states and native system saves. Other special system preference files could be also saved here.
