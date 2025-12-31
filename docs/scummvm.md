# ScummVM

## Game launcher files

ScummVM supports `.svm` and `.scummvm` launcher files. You can create an empty file with one of these extensions and place it inside the game folder. You can even use any file name, since ScummVM can detect the game from the files in the folder.

For example, you could create an empty `Day of the Tentacle.svm` file, place it inside the game folder, and that is it.

## Default `scummvm.ini` configuration file

```ini
[scummvm]
autosave_period=300
mute=false
gui_theme=replayos
native_mt32=false
gui_use_game_language=false
confirm_exit=false
mt32_device=fluidsynth
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
;soundfont=/media/<unit>/bios/scummvm/soundfonts/GM_Roland.sf2
;soundfont=/media/<unit>/bios/scummvm/soundfonts/FluidR3_GM.sf2
;soundfont=/media/<unit>/bios/scummvm/soundfonts/UHD3.sf2
music_volume=256
speech_mute=false
lastselectedgame=tentacle
music_driver=auto
opl_driver=auto
versioninfo=2.8.0git
speech_volume=192
gui_language=en
enable_gs=true
```

## Change MIDI soundfont

To change the MIDI soundfont used by the games, follow these steps:
1. Open the `scummvm.ini` file stored in your bios folder
2. Search for the `soundfont` parameter
3. If the parameter is commented with `;`, remove the `;`
4. Set one of the four MIDI soundfonts available in the BIOS folder:
```ini
soundfont=/media/<unit>/bios/scummvm/soundfonts/Roland_SC-55.sf2
soundfont=/media/<unit>/bios/scummvm/soundfonts/GM_Roland.sf2
soundfont=/media/<unit>/bios/scummvm/soundfonts/FluidR3_GM.sf2
soundfont=/media/<unit>/bios/scummvm/soundfonts/UHD3.sf2
```
5. Replace `<unit>` above with `sd`, `usb`, `nfs`, or `nvme` depending on the storage device you are using
6. Save the file and restart the game
