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

Whether you are using the internal the MicroSD exFAT partition, USB unit or NFS share, the system will create the following folder structure inside any of these folders:

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
│   ├── atari_2600
│   ├── atari_5200
│   ├── atari_7800
│   ├── atari_jaguar
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
│   └── sony_psx
├── config
│   ├── input
│   │   ├── game
│   │   │   ├── crt
│   │   │   └── lcd
│   │   └── system
│   │       ├── crt
│   │       └── lcd
│   └── settings
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
│   ├── atari_2600
│   ├── atari_5200
│   ├── atari_7800
│   ├── atari_jaguar
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
│   └── sony_psx
└── saves
    ├── alpha_player
    ├── amstrad_cpc
    ├── arcade_dc
    ├── arcade_fbneo
    ├── arcade_mame
    ├── arcade_mame_2k3p
    ├── arcade_stv
    ├── atari_2600
    ├── atari_5200
    ├── atari_7800
    ├── atari_jaguar
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
    └── sony_psx
```

## bios folder
It is where all system BIOS, arcade samples, sound fonts, computer special core configurations, and any other special system file are stored.

## captures folder
This is the place where screenshots are stored.

## config folder
This is where all input and core configurations are saved. The different configurations can be applied to the entire system, specific games, or particular types of TVs, whether LCD or CRT.

## roms folder
This is where you can copy your game files. The system folders are prefixed by the company name for better categorization. Additionally, there are special system folders prefixed with an underscore, such as [`_autostart`](autostart.md), `_extra`, `_favorites`, and `_recent`.

## saves folder
This folder contains all user save states and native system saves. Other special system preference files could be also saved here.
