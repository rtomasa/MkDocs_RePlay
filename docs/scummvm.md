# ScummVM

## Game launcher files

ScummVM supports `.svm` and `.scummvm` launcher files. You can create an empty file with either of these extensions and place it inside the game folder. The file name can be anything, as ScummVM detects the game based on the contents of the folder.

For example, you can create an empty file named `Day of the Tentacle.svm`, place it in the game folder, and that is all that is required.

## M3U playlists (single‑entry and folders)

You can also use `.m3u` playlists to launch ScummVM games. Single‑entry m3u files are resolved to the referenced content (relative paths are supported), and the referenced files/folders are hidden from the UI to keep the list clean.

Example `Day of the Tentacle.m3u` content (relative path):

`./tentacle/tentacle.svm`

**Notes**:

* Single‑entry m3u playlists launch the referenced file directly.
* Multi‑entry m3u playlists are kept intact for multi‑disc systems.

## Recommended `scummvm.ini` configuration file

```ini
[scummvm]
autosave_period=300
mute=false
native_mt32=false
gui_use_game_language=false
confirm_exit=false
mt32_device=mt32
gui_scale=200
gui_return_to_launcher_at_exit=false
gui_disable_fixed_font_scaling=false
subtitles=true
multi_midi=true
fullscreen=true
gui_renderer=normal
gm_device=auto
sfx_volume=192
;soundfont=/media/<unit>/bios/scummvm/soundfonts/Roland_SC-55.sf2
music_volume=256
speech_mute=false
music_driver=auto
opl_driver=auto
speech_volume=192
gui_language=en
enable_gs=true
```

## About General MIDI music

By using the above configuration, the system will automatically use Roland SC-55 music when the [additional required BIOS files](addbios.md#minimum-bios-system-files) are present and the game supports it. No additional configuration is required.

## About Roland MT-32 music

By using the above configuration, the system will automatically use Roland MT-32 music when the [additional required BIOS files](addbios.md#minimum-bios-system-files) are present and the game supports it. No additional configuration is required.

## Changing the MIDI soundfont manually

For games that support only General MIDI (GM), you can select a different soundfont instead of the default (and recommended) Roland SC-55.

To change the MIDI soundfont used by games, follow these steps:

1. Open the `scummvm.ini` file located in your BIOS folder.
2. Search for the `soundfont` parameter.
3. If the parameter is commented out with `;`, remove the `;`.
4. Set one of the four MIDI soundfonts available in the BIOS folder:

   ```ini
   soundfont=/media/<unit>/bios/scummvm/soundfonts/Roland_SC-55.sf2
   soundfont=/media/<unit>/bios/scummvm/soundfonts/GM_Roland.sf2
   soundfont=/media/<unit>/bios/scummvm/soundfonts/FluidR3_GM.sf2
   soundfont=/media/<unit>/bios/scummvm/soundfonts/UHD3.sf2
   ```
5. Replace `<unit>` with `sd`, `usb`, `nfs`, or `nvme`, depending on the storage device in use.
6. Save the file and restart the game.

**NOTE**: You may copy additional soundfont files into the same directory if you wish to use them.
