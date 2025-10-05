# Changelog

<!--
# v0.59.0 (RC5)
- [X] Added support for mounting NFS shares using either DNS hostnames or IP addresses
- [X] Added Wi-Fi WPA2/WPA3 support.
- [X] Changed system label from `SNK NEO-GEO (AES/MVS)` to `SNK NEO-GEO` to clarify that it refers only to the console system
- [X] Increased system root partition size from 3GB to 7GB to prevent issues during updates, driver installations, and package management
-->
# v0.58.0 (RC4)
- [X] Added support for new bitmask input engine for digital controllers (`RETRO_ENVIRONMENT_GET_INPUT_BITMASKS`):
    - Lower CPU overhead: instead of cores asking input state 12-16 times per frame per port, they call it once and get all button states in a single call.
    - Consistent snapshot: all button states come from the same poll cycle, eliminating per-button timing skew, matching real hardware behaviour.
    - Less input latency: cores skip dozens of callback round-trips per frame. The improvement is small but measurable compared to traditional per-button polling.
- [X] Added new `CRT STABILITY BOOST` option (enabled by default) for improved image stability
- [X] Added new `FOLDER REGENERATION` option to enable/disable system rom folder regeneration of every boot
- [X] Added support for DIY Tilt Input device addon to automatically rotate the UI and filter vertical games
- [X] Added new XBOX driver installer in extras
- [X] Changed generic DAC Color Range autodetection for known DAC models
- [X] Changed black screensaver by ambiscan color cycle to prevent confusion with the Pi being powered off
- [X] Fixed unwanted button press after resume, save/load state and extra cores
- [X] Fixed `SWAP UI A/B BUTTONS` input option affecting keyboard

# v0.57.0 (RC3)
- [X] Fixed generic video DAC autodetection
- [X] Updated all system cores

# v0.56.0 (RC2)
- [X] Added DynaRes LCD NRR (Native Refresh Rate) option
    - Standard LCD screens run at 55-61Hz
    - LCD VRR screens run at 48-75Hz
- [X] Added Wi-Fi configuration to replay.cfg
- [X] Removed MAME2K3+ from Pi5
- [X] Removed CRT overscan reduction causing DAC image stability issues
- [X] Improved Power Button detection
- [X] Fixed system options text truncation
- [X] Fixed `SET_SYSTEM_AV_INFO` not updating aspect ratio and refresh rate
- [X] Fixed Alpha Player:
    - Fixed geometry and av_info calls
    - Fixed aspect ratio
    - Fixed image stability and timings

# v0.55.0 (RC1)
- [X] Fully refactored DRM init mode
    - Added HDMI hotplug detection
    - Added HDMI CEC support
    - Added HDMI DPMS restart sequence
- [X] Added a new graceful implementation for poweroff, reboot, and exit events
- [X] Added N64 and DC to `BOOT TO SYSTEM` option
- [X] Added optional custom xone and xpad drivers installers to RePlay Extra section
- [X] Updated custom GCon2 and TAITO drivers to update automatically on kernel updates (DKMS)
- [X] Updated Alpha Player to use standard VESA video mode when connected to 31kHz monitors
- [X] Updated screen test utility image to make easier to identify limited color range issues
- [X] Fixed bug where Alpha Player advanced to the next playlist entry before current file ended
- [X] Fixed crash in Alpha Player when encountering a missing file in M3U playlist
- [X] Fixed crash on `BOOT TO SYSTEM` option when the system is not visible
- [X] Fixed scanlines option not properly enabled in 31kHz mode
- [X] Fixed a bug that caused mappings and input descriptors to load and refresh incorrectly after selecting different controller types
- [X] Removed pre-installed custom xone and xpad drivers due to some regression and compatibility issues.

# v0.54.0 (Sixth Private BETA)
- [X] Added new alpha-player media core
- [X] Added frontend support for the new alpha-player media core
- [X] Added a new RGB color range setting for TVs or DACs that do not support full-range RGB output
- [X] Added support for RPi5 NVMe PCIe storage units (system cannot boot from NVMe)
- [X] Added new custom xone and xpad drivers (thanks to Kev - forkymcforkface)
- [X] Changed arcade rotation visibility option to filter any horizontal or vertical game of any rotation mode
- [X] Fixed bug in system core options hiding one of the core options randomly
- [X] Fixed screensaver displaying last color used by ambiscan
- [X] Fixed scanline filter option not disabled on all unsupported modes
- [X] Fixed Retroflag Reset button functionality
- [X] Fixed poweroff and reboot not unloading game and core in all scenarios
- [X] Fixed multiple audio DACs issues taking priority over hdmi one

# v0.53.0 (Fifth Private BETA)
- [X] Refactored DynaRes to perform faster video mode switching using atomic or nonatomic operations based on the Pi model
- [X] Added new AmbiScan color decoration effect (enabled by default)
- [X] Added comfort noise generation (CNG) to the RePlay Menu Core to prevent smart speakers from entering standby mode during silence
- [X] Added support for refreshing the RePlay Menu Core when rotating the UI
- [X] Added per-system and per-game configuration support for scanlines filters
- [X] Improved Raspberry Pi model detection used across various system features
- [X] Improved shutdown functionality for safer and faster poweroff and reboot operations
- [X] Changed Nintendo DS core to melonDS DS
- [X] Changed Linux CLI locale to English for consistent system lang output
- [X] Changed the sound normalizer engine (suggested test games: *Batsugun* for loud, *The Punisher* for quiet)
- [X] Changed the `INITIAL REFRESH RATE` UI option to the new `CRT SCREEN MODE`
- [X] Updated Flycast core to the latest available version
- [X] Fixed screen test core not properly updating texture size on mode switch
- [X] Fixed screen rotation and mirroring issues in hardware-accelerated 3D games
- [X] Fixed a macroassembler bug in Flycast causing audio issues on ARM64 devices
- [X] Fixed initialization and deinitialization bugs in the audio resampler that could lead to random crashes
- [X] Fixed `usercontrollerdb.txt` not being refreshed when mounting different drives
- [X] Fixed SRAM native save data not being properly written during reboot or power-off events
- [X] Fixed audio resampler clipping that occurred in specific scenarios
- [X] Fixed an issue where audio device selection could fail when booting with a USB audio DAC connected
- [X] Fixed a bug where unplugging the controller during physical mapping caused the UI to become unresponsive
- [X] Removed the general 20% volume reduction workaround for audio clipping, as it's no longer necessary

# v0.52.0 (Fourth Private BETA)
- [X] Refactored UI file browser engine for better performance
- [X] Added new `SYSTEM > UI PAUSES GAME` option to pause game while the UI is open (now defaults to OFF)
- [X] Added new game image rotation engine so that now cores like FBNeo can rotate the screen via core option
    - Added proper aspect ratio calculation in games that are rotated 90 or 270 degrees
- [X] Added experimental 2K and 4K (Pi 5 only) screen modes. Please be aware that enabling these modes may result in known video issues, increased heat, and higher power consumption, potentially reducing Pi performance and causing problems with external drives
- [X] Added a "Crop Mode" option in PSX system settings, enabling users to set it to "All Borders" as a workaround for PSX PAL games displaying a black screen
- [X] Added new `REPLAY OPTIONS > VISIBILITY` menu group
    - Moved here all previous `SYSTEM > UI SHOW *` options
    - Added four new arcade specific option filters:
        - Number of Players
        - Screen Rotation
        - Number of Screens
        - Number of Buttons
- [X] Added automatic initialization of all audio hardware mixers to 100% volume
- [X] Added ability to mix analog and digital buttons in core virtual input mappings
- [X] Added and updated internal arcade naming database based on MAME 0.276
- [X] Added dead zone handling for analog sticks and threshold detection for trigger buttons
- [X] Changed analog stick processing to radial dead zone for improved accuracy and full-range movement (fixes some cores)
- [X] Changed ScummVM core for better Libretro integration and updated to latest version. Fixes issues with games like:
    - Leisure Suit Larry VII (CD Spanish)
    - Escape from Monkey Island (CD Spanish)
    - Cruise for a Corpse (DOS Spanish)
- [X] Changed wrong default PSX default settings
- [X] Changed Flycast core to latest stable realease due to an audio regression issue
- [X] Changed M3U limit from 320 to 1024 files per folder (fixes X68K massive romset)
- [X] Changed scanlines UI info message for clarity (Integer Scale V and Raspberry Pi4 or newer required)
- [X] Changed `REBOOT` and `POWER OFF` functions to perform the actions in a graceful way, preventing potential data loss
- [X] Changed save state folder structure to match rom folder structure
- [X] Fixed several inaccuracies in X/Y position calculations for both games and UI
- [X] Fixed video drop issues caused by system allowing default resolutions higher than 1920x1080 in `CRT/LCD AUTO` screen mode
- [X] Fixed bug in UI file extension check exceeding max number of valid extensions
- [X] Fixed NFS mount not persisting on reboot
- [X] Fixed NFS UI corruption due to NFS v4 never guarantees d_type
- [X] Fixed UI corruptions when reading UTF-8 filesystem chars
- [X] Fixed autostart crashing when rom file does not exists
- [X] Fixed DosBox-Pure core crashing in some games due to a bug with the disney sound system
- [X] Fixed Caprice32 (CPC) core displaying the M3U file in the list of available disks
- [X] Fixed video info displaying wrong Hz information for some cores/games
- [X] Removed `CRT 640X480@NRR` video mode. The system is already able to properly manage the screen mode based on the CRT Type selected
- [X] Removed Pi3/3+/Zero 2 default overclock due to instability issues (can be re‑enabled easily via config.txt)
- [X] Removed unwanted and non-working PSX core options
- [X] Removed unwanted and non-working N64 core options
- [X] Removed `STORAGE SAFE MODE` due to poor performance and the potential to shorten the lifespan of SD cards and USB storage devices

# v0.51.0 (Third Private BETA)
- [X] Added new "Arcade & PC 31kHz" monitor mode. This new mode enables the following features:
    - Play 15kHz content on 31kHz monitors
    - Play MS-DOS games at native 70Hz modes (requires disabling force 60fps in core settings)
    - Play hi-res interlaced games (DC, PSX, Saturn, etc.) in progressive
    - Enable or disable scanlines as desired
- [X] Added new `LCD 1024x768@70Hz` video mode for native MS-DOS experience (requires disabling force 60fps in core settings)
- [X] Added scanline options for "Arcade & PC 31kHz" CRT type mode
- [X] Added new fully BLACK scanline option (perfect for 31kHz mode)
- [X] Added missing Ctrl, Alt, Shift keyboard key support (now you can play MS-DOS properly)
- [X] Added new PiBench core for CPU/GPU performance measurement
- [X] Added ability to disable vsync internally at video engine level (used by PiBench)
- [X] Added missing support for analog buttons in ANALOG mode causing also crashes in some cores (A2600, PSX, DC)
- [X] Changed system boot sequence, reducing startup time a few seconds
- [X] Changed (refactored) video engine for improved compatibility with different CRT monitor types
- [X] Changed UI browser to show file type as info instead of extensions (cleaner look and easier identification)
- [X] Changed M3U limit from 256 to 320 files per folder
- [X] Changed Pi3 PSX core options for improved compatibility and performance
- [X] Fixed HDMI LCD video init not properly selecting default 60Hz mode
- [X] Fixed scanlines being displayed when vertical game resolution is equal to native screen resolution
- [X] Fixed `ARCADE 15/25/31KHZ` CRT type mode
- [X] Fixed crash caused by cores reporting more than 6 ports (PSX, DC)
- [X] Fixed DynaRes prioritizing interlaced over progressive modes on PC/31 kHz monitors
- [X] Fixed LCD DRR modes crashing
- [X] Fixed System > Information > Resolution options not displaying native monitor refresh
- [X] Fixed system image creation tool so that it can be now written using the official Raspberry Pi Imager

# v0.50.2
- [X] Improved DC/NAOMI image scaling quality in LCD

# v0.50.1
- [X] Added more available values to the Screen Position X/Y option

# v0.50.0 (Second Private BETA)
- [X] Added internal core version verification
- [X] Updated MAME core to v0.275
- [X] Updated Flycast core to v2.4
- [X] Changed UI file explorer to automatically hide folders with arcade rom names
- [X] Fixed recents not properly handling favorites
- [X] Fixed crash when core is not properly identified
- [X] Fixed saves, bios, assets cache path issue and memory leak

# v0.49.23
- [X] Fixed no sound when booting a game with audio normalization enabled and core starts with total silent

# v0.49.22
- [X] Fixed scanline shader not applied when UI menu is opened

# v0.49.21
- [X] Fixed handheld aspect ratio in CRT mode (also fixes Atari Lynx black screen)

# v0.49.20
- [X] Added modern disk control API v1 to blueMSX core
- [X] Fixed frontend support for old disk control API v0
- [X] Fixed input descriptor infinite loop execution bug

# v0.49.19
- [X] Added dual screen DB info to Soccer Superstars
- [X] Fixed RePlay menu core booting with incorrect video mode after system crash
- [X] Fixed RePlay menu core booting in infinite loop after system crash
- [X] Fixed MAME random performance degradation
- [X] Fixed games displaying black screen when its resolution is higher than the TV's native one

# v0.49.18
- [X] Changed RePlay menu core
    - Fully refactored code to make standarized use of libretro API
    - Fully integrarted images (no more external SDL and PNG file dependencies)
    - Color mode is now 32bit XRGB8888
- [X] Fixed flycast core not properly reseting static variables when dynamic library is unloaded. This caused the frontend to crash due to input descriptors never reloaded.

# v0.49.17
- [X] Fixed a bug when UTF8 chars are used in the core system settings

# v0.49.16
- [X] Changed Screen Test core utility
    - Fully refactored code to make standarized use of libretro API
    - Fully integrarted images (no more external SDL and PNG file dependencies)
    - Color mode is now 32bit XRGB8888
- [X] Fixed chash for cores not having any system setting

# v0.49.15
- [X] Added proper color conversion 0RGB1555 (fixes MAME Virtua Racing)
- [X] Fixed bug in `SET_INPUT_DESCRIPTORS` and MAME 2K3+

# v0.49.14
- [X] Changed the options info text to blue color for better differentiation

# v0.49.13
- [X] Added new system functionality to write frontend events into /var/log/replay.log
- [X] Changed shutdown functionality to properly handle system signals (like soft poweroff)
- [X] Fixed gamepad initialization bug in Dreamcast system

# v0.49.12
- [X] Added new input option to allow all users to control de UI
- [X] Added help hint when hovering over Controller Mapping menu option entry

# v0.49.11
- [X] Added a new additional 8Bitdo M30 default SDL mapping
- [X] Fixed bug in Controller Mapping caused by some controllers having an axis and a buttom mapped to one single physical button

# v0.49.10
- [X] Removed timeout in Test Physical Button and Controller Mapping options.
    - Mapped buttons can now skip mappings when pressed
    - Keyboard space key now also skip mappings when pressed

# v0.49.9
- [X] Fixed a bug in the keyboard controller preventing the Test Physical Button and Controller Mapping options from working properly

# v0.49.8
- [X] Fixed RGB-Pi 2 (prototype) autodetection and initialization

# v0.49.7
- [X] Added .jag file extension support to Atari Jaguar system

# v0.49.6
- [X] Fixed custom controller mappings not loading for several cores and crashing the system randomly

# v0.49.5
- [X] Fixed and refactored the new RGB-Pi 2 DAC init system which was also preventing all RPi4 models from booting

# v0.49.4
- [X] Fixed chash in forders having a big number of m3u files
- [X] Fixed a bug where frontend crashes when trying to open a corrupted rom file

# v0.49.3
- [X] Fixed Home button UI mapping

# v0.49.2
- [X] Disabled Scanline option on Pi3 family due to lack of support for native OGL ES3

# v0.49.1
- [X] Changed coinop countdown to work also when UI is opened.
- [X] Fixed coinop chrashing the system on boot when enabled

# v0.49.0 (First Private BETA)
- [X] Major input manager engine refactor:
    - Added new option to create SDL native physical mappings (XBOX based mappings)
    - Added new Device Port option to redirect controllers to other ports (e.g. P2 can also control P1)
    - Changed Test Button option to display SDL logical button name + SDL physical Id
    - Changed core input remap so that now it is based on the new SDL logical names
    - Changed core input remap so that now it is simplified to only display the current player buttons
    - Changed input remap indicator to simply display if a remap file is in use
    - Fixed UI so that remaps only apply to games
    - Fixed Device Type option not properly applying the user selections
    - Fixed Remap Button options not properly applying the user selections
    - Fixed many bugs in save_input_cfg function
    - Fixed many bugs in load_input_cfg function
    - Removed `LEFT STICK TO DPAD` option since it was confusing and it is not required with the new physical mappings
    - Removed `BUTTONS TO TRIGGER` option since it was confusing and it is not required with the new physical mappings
- [X] Changed vanilla ScummVM by RePlayOS fork

## v0.48.4
- [X] Fixed input test button timeout

## v0.48.3
- [X] Changed DRM default video mode detection before SDL initialization for improved HDMI audio handshake 

## v0.48.2
- [X] Added internal gamepad layout detection for future uses

## v0.48.1
- [X] Fixed small bug on DAC init 

## v0.48.0
- [X] Added new refactored input engine to better support different input devices and fix some bugs
- [X] Added new keyboard engine supporting poll, event, and text modes
- [X] Added new keyboard option to set keyboard in real or command modes
- [X] Added NDS in single screen mode
- [X] Added NDS in CRT screen mode
- [X] Changed native initialization interface for the RGB-Pi 2 Prototype
- [X] Changed GB/GBC into two sepparated systems
- [X] Changed Nintendo DS default screen option to "Bottom Only"
- [X] Changed Amstrad CPC combo button to B to avoid frontend menu combo conflict
- [X] Changed keyboard UI menu button to Windows Key for avoiding key conflicts
- [X] Fixed Commodore 64 core to properly announce RetroPad default controller info
- [X] Fixed Commodore 64 default file mapping buttons
- [X] Fixed XRGB8888 video corruption in some cores
- [X] Fixed game dual screen stacked filter not working properly
- [X] Fixed Amstrad CPC audio (core_audio_sample was not implemented)
- [X] Fixed aspect ratio not set automatically when selecting dual screen modes
- [X] Fixed a small bug where the video engine was not checking if second screen was initialized
- [X] Fixed core default input type not set when new controller device is connected
- [X] Removed Esc (exit) command when frontend is compiled in release mode

## v0.47.0
- [X] Refactored GL texture management to make use of native XRGB8888 and BGR color conversion for improved video quality and performance

## v0.46.4
- [X] Fixed OpenGL pixel format warning due to incomplete texture deinit

## v0.46.3
- [X] Improved performance when doing software based XRGB8888 to RGB565 color conversion

## v0.46.2
- [X] Removed Alpha-Player core until new re-work is completed
- [X] Changed media_player folder name to alpha_player

## v0.46.1
- [X] Replaced color blind option by independent RGB color scale values

## v0.46.0
- [X] Added new native initialization interface for the RGB-Pi 2 Prototype
- [X] Added new option to set different CSYNC modes (Separated H/V, Csync (AND), Csync (XOR))
- [X] Added new gamma video option
- [X] Added display name and vendor in system information
- [X] Changed N64 Emulation profiles (now Quality in Pi5 enables LLE Unfiltered)
- [X] Fixed Xbox 360 Controller triggers
- [X] Fixed missing package libgpiod-dev required by RetroFlag Pi5 Case

## v0.45.0
- [X] Added new audio device options (hdmi, gpio dac (hifiberry), usb dac)
- [X] Added new set of aspect ratio and scalling modes
- [X] Added new set of scan line modes
- [X] Added support for additional Controllers
- [X] Added support for Retroflag Pi5 cases
- [X] Changed GPIO Joy overlay to [Pi5] section in config.txt
- [X] Changed default N64 system options for improved performance
- [X] Fixed bug where system needed two reboots to get sound when using the same SD in another Pi model

## v0.44.1
- [X] Changed Default aspect ratio on 16/9 TVs to 4/3 instead of Native to avoid games with anamorfic resolutions (e.g. 704x224) look streched

## v0.44.0
- [X] Added new sound option to enable experimental volume normalization engine
- [X] Changed UI navigation page limit to 999 items

## v0.43.1
- [X] Fixed bug where system settings was missing one entry in all cores

## v0.43.0
- [X] Added new gpio-joystick driver for Jamma arcade boards
- [X] Added improved USB external drive mount engine
- [X] Added new `LOW LATENCY MODE` option to both global and system/game settings
- [X] Added new gamepads support
- [X] Added CHD back to NGCD supported games and removed CCD
- [X] Changed to NeoCD core for NeoGeo CD system
- [X] Changed logic to disable some CRT-only options when using LCD
- [X] Fixed driver support for TAITO Paddle & Trackball
- [X] Fixed driver support for NAMCO GunCon 2 Lightgun
- [X] Fixed game/system input config file not properly loaded on start or restart games

## v0.42.0
- [X] Added proper video memory flush when loading/unloading games and/or resolution changes
- [X] Added ZX Spectrum libretro core proper PAL & NTSC resolutions
- [X] Added kernel parameter to avoid USB gamepad autosuspend
- [X] Added ability to load custom SDL mapping DB file from <unit>/config/input/sdlusermapsdb.txt path
- [X] Updated retro-bit Sega Saturn SDL mappings
- [X] Updated 8bitdo NeoGeo SDL mappings
- [X] Changed default DC BIOS from HLE to Real BIOS due to some game compatibility issues
- [X] Changed default PSX BIOS from fast to normal BIOS due to some game compatibility issues
- [X] Changed PSX core options to avoid interlacing artifacts when using LCD screens
- [X] Changed 3DO Threaded DSP to disabled due to some game compatibility issues
- [X] Fixed screensaver
- [X] Fixed sound mono downmix not working
- [X] Fixed scan line system and core options not working properly
- [X] Fixed dual screen to avoid enabling the option until system reboot
- [X] Fixed scan lines filter on pixel perfect aspect ratio
- [X] Fixed video reinit speed regresion back again to 1-3 frames speed
- [X] Removed NeoGeo CD listing CHD games since FBNeo does not support CHD format due to licensing conflict
- [X] Removed temporary code for RGB-Pi 2 Prototype initialization from automatic video mode option (moved to manual)

## v0.41.0
- [X] Added a newly fully refactored A/V sync engine, now based on the audio master clock
- [X] Added temporary code for RGB-Pi 2 Prototype initialization
- [X] Updated to new kernel 6.6.62 with support for RPi500
- [X] Changed Dreamcast emulation profiles for improved performance
- [X] Changed "Emulation Quality" to "Emulation Profile"
- [X] Changed method used for calculating realtime FPS
- [X] Removed audio resampler default volume reduction
- [X] Fixed a regression bug with XRGB8888 color conversion

## v0.40.3
- [X] Added black screen screen saver
- [X] Refactored OpenGL code and performed some code clean up

## v0.40.2
- [X] Changed DC RPi5 performance profile
- [X] Removed "Reset All System Configs" option from user compilation (only available in debug mode)
- [X] Fixed bug loading emulation quality profiles

## v0.40.1
- [X] Updated to new kernel 6.6.51 containing many video improvements making interlaced modes much more stable
- [X] Fixed some games and systems not displaying any image due to the use of odd resolutions

## v0.40.0
- [X] Fixed core OpenGL video context reinit (fixes DC Full Framebuffer Emulation in CRT)
- [X] Fixed DC interlaced drawing fields for improved image stability in some games
- [X] Fixed non-working interlaced PAL resolutions
- [X] Fixed silent boot

## v0.39.0
- [X] Added new option to boot into PAL 50 or NTSC 60 mode (useful for some CRT only PAL TVs)
- [X] Added GPU Frequency in System Information option menu
- [X] Added option to reset all system configurations (frontend, cores, and input)
- [X] Changed Default video mode option to CRT/LCD Auto
- [X] Changed all predefault overclock settings for better stability
- [X] Changed Emulation Quality options to Performance, Balanced, and Quality
    - Automatically adjusts core options based on RPi model, and Emulation Quality selected option
- [X] Fixed bug making P1 controlling P2
- [X] Fixed function for getting interlaced video modes in CRT mode 
- [X] Fixed A/V sync in NRR mode in systems running internally at different speed rates
- [X] Fixed A/V reinit in OpenGL based cores when running in CRT in RPi5
- [X] Fixed Screen Test core crashing due to bad compilation
- [X] Fixed firstboot auto-configuration
- [X] Fixed a bug hiding some input options in system menu
- [X] Fixed OpenGL frontend texture sizing bug (fixes DC Full Framebuffer Emulation in LCD)
- [X] Fixes PSX graphic glitches in Oddworld games

## v0.38.0
- [X] Added support for new Raspberry Pi 5 2GB model
- [X] Added ARM64 performance compilation flags
- [X] Added new mono downmix audio option
- [X] Added 60/50Hz Screen Test button toggle
- [X] Added support for many new gamepads and joystics
- [X] Added 5 connection retries with 2 seconds of retry interval for NFS mounting
- [X] Added frontend autoreload functionality on crash
- [X] Updated Amiga Core (2024-09-16). Fixes some game crashes and issues
- [X] Changed Favorites, Recents and Autostart files from absolute to relative paths
- [X] Changed default Linux kernel joystick polling rate to 1ms
- [X] Fixed `RETRO_ENVIRONMENT_SET_SYSTEM_AV_INFO` refresh rate change detection
- [X] Fixed initialization of some gamepad and joysticks (E.g. Astro City Mini)
- [X] Removed login service for improved boot experience and speed

## v0.37.0
- [X] Added HDMI LCD video mode check to make use of progressive resolutions only
- [X] Added power off option (its use is optional)
- [X] Added seven extra skin slots for user custom skins
- [X] Added satellaview missing BIOS to new official pack
- [X] Added fds missing BIOS to new official pack
- [X] Added SD fallback functionality when USB is removed without umounting
- [X] Added ability to set best built-in core settings based on Pi family (E.g. default DC alpha sorting on Pi4/Pi5)
- [X] Updated all cores (2024-08-30)
- [X] Changed boot and system mount points to secure write mode
- [X] Changed default overclock from 2900 to 2800 because some Pi5 not booting
- [X] Changed video mode text list for better readability
- [X] Changed default NDS touch control to Joystick
- [X] Changed predefault performance emu options for N64 and DC in Pi5
- [X] Fixed Aero Blasters PCE crash
- [X] Fixed crash loading Screen Test extra core after playing cores with multy CD support
- [X] Fixed crash loading frontend UI after core not able to load content
- [X] Fixed UI search index buffer overflow
- [X] Fixed custom GCon2 screen flash in DC
- [X] Removed Atari ST due to many emulation and performance issues
 
## v0.36.0
- [X] Added RePlay script updater
- [X] Refactored script launcher
- [X] Refactored timezone functionality
- [X] Refactored reboot functionality

## v0.35.0
- [X] Added script to create user sd FAT partition on first boot
- [X] Added option to show/hide arcade, consoles, computers, handhelds
- [X] Added verbose system option only when frontend is compiled in DEBUG mode
- [X] Fixed MSX BIOS check

## v0.34.0
- [X] Added support for special RePlay Extra cores and scripts
- [X] Added Screen Test extra core (color and geometry)
- [X] Added BIOS script downloader
- [X] Added USB disk I/O performance improvements
- [X] Added storage safe mode (requires manual remount)
- [X] Added custom GCon2 screen flash for improved precision
- [X] Fixed system volume in RPi3 model

## v0.33.0
- [X] Added DynRes interlaced video mode support for Raspberry Pi 3, 4 and 5
- [X] Added Raspberry Pi 3 CRT support for PSX, X68K, IBM PC and SCUMMVM
- [X] Added option to enable/disable overscan reduction in CRT screens
- [X] Added CRT dual screen support
- [X] Added new dual screen UI game filter (stacked and side-by-syde)
- [X] Added UI game filter auto selection on dual screen mode selection
- [X] Added NDS support in CRT mode (only in dual screen stacked mode)
- [X] Added support for 6 players
- [X] Added USB storage support (FAT/FAT32/exFAT)
- [X] Added NFS storage support
- [X] Added bios check when loading games
- [X] Added new RePlay Extra folder
- [X] Added option to autodetect and set time zone (useful for save state names)
- [X] Added new driver support for TAITO Paddle & Trackball
- [X] Added new driver support for NAMCO GunCon 2 Lightgun
- [X] Added initial support for keyboard scancode core inputs (required for MAME TAB OSD)
- [X] Fixed several UI zoom scaling issues
- [X] Fixed RePlay core background tiling and zoom now based on screen resolution
- [X] Fixed screen capture in CRT dual screen modes
- [X] Fixed crash when there are no joysticks connected on loading games
- [X] Fixed UI Game Filter not working with Favorites and Recent games
- [X] Fixed incorrect port device type assigment
- [X] Fixed Replay UI core zoom factor in hi-res modes
- [X] Removed forced CRT 50/60Hz modes due to compatibility and stability issues

## v0.32.3
**IMPORTANT!!! This is the last version containing development code for old RGB-Pi GPIO/DPI standard A/V**
- [X] Fixed bug in audio resampler dynamic audio pitch in single-thread cores

## v0.32.2
- [X] Fixed Raspberry Pi 5 OpenGL core support
- [X] Fixed audio resampler dynamic audio pitch
- [X] Fixed audio not init when moving SD to another different Pi model

## v0.32.1
- [X] Fixed aspect ratio in some systems due to OpenGL texture assigment error when setting game geometry
- [X] Fixed random crash loading systems due to disk control interface not being properly freed

## v0.32.0
- [X] Added new DynaRes 2.0 engine
    - Support for multiple LCD and CRT initialization modes
    - Ability to load system without any connected monitor
    - New screen mode option to set resolution
    - New CRT type option to set monitor type
    - CRT support for all RPi 3, 4 and 5 models (RPi 3 support is limited)
    - RPi3 won't display/support systems running interlaced modes in CRT mode
    - Updated modeline calculator based on latest version of Calamity's SwitchRes
    - Added DRR (Dual Refresh Rate) 60/50Hz support for both CRT and LCD displays
    - Set default HDMI mode to 60hz (max FHD 1080)
    - Enhanced capability for ultra-fast on-the-fly timing adjustments within 1-3 frames Vs. 108-120 frames in DynaRes 1.0
    - Added handheld CRT lowres support
- [X] Added new scalling modes:
    - Integer Scale Overscan (only works in FHD 1080! nearly the original overscan of a CRT)
    - Integer Scale Underscan (useful for special DIY projects)
- [X] Added new functionlity to RePlay start menu core
    - It now properly manage all diferent video modes at boot
    - Fixed background scaling in dual screen modes
    - Fixed background rendering when changing dual screen modes from UI
    - Improved performance
    - Background rotation
    - Uses its own native aspect ratio different from other cores
- [X] Added current resolution in information option
- [X] Added automatic roms folder creation functionality
- [X] Added per system/game X/Y position
- [X] Improved X/Y position option to automatically scale based on current resolution
- [X] Improved audio and video per frame speed accuracy and synchonization
- [X] Fixed core speed when running multithread cores
- [X] Fixed crash when changing a RePlay option from game menu
- [X] Fixed bug loading custom paths from cfg file
- [X] Fixed UI scaling in dual screen vertical mode
- [X] Fixed game input remaps affecting UI button actions

## v0.31.0
- [X] Added virtual disk engine
- [X] Added filter to hide all files contained in a M3U file
- [X] Added initial support for Egret II mini spinner/trackball controller (NOT TESTED)
- [X] Added input option for checking button IDs when pressed
- [X] Changed option Shoulders to Triggers (digital to analog) to Buttons to Triggers supporting 3 configurations:
    - Buttons 1/2 - Useful in arcade/jamma
    - Buttons 2/3 - Useful in arcade/jamma
    - Buttons 9/10 (L/R) - Useful in arcade/jamma and SNES like gamepads
- [X] Changed all "Reset ..." option labels to "Remove ..."
- [X] Fixed save/load slot name not updated when overrided
- [X] Fixed core crashes due to a bug in `RETRO_ENVIRONMENT_SET_MESSAGE`
- [X] Fixed save/load crash getting label 
- [X] Fixed save/load name display lenght

## v0.30.0
- [X] Added new system core remapping engine
- [X] Added support for Raspberry Pi Zero 2
- [X] Added Shoulders to Trigger (digital to analog) to both system and game input option menu. (e.g. allows playing Outrun using digital controls)
- [X] Added Left Stick to DPAD (analog to digital) to both system and game input option menu
- [X] Added option to hide Media Player
- [X] Changed some RePlay UI design patterns
    - Added .. entry in systems if not in menu core
    - Added replay options entry in systems if in menu core
    - Added replay options entry in system menu
    - Added .. entry in replay options (same action cmd as start btn)
    - Changed input and settings labels in system menu
    - Changed home btn as quick direct access back to system menu if not in menu core
    - Removed thread titles to improve readability and performance
    - Removed start action cmd
    - Removed start ui labels
    - Removed core name info inside all system settings
- [X] Changed Kiosk hardcoded values to whitelist
- [X] Fixed performance issue in Replay options > video menu

## v0.29.0
- [X] Added global mouse support
    - Only one mouse is currently supported
    - Mouse works no matter the player number or port
- [X] Added start button emulation via middle mouse button (opens ScummVM menu)

## v0.28.0
- [X] Added new Media Player system (alpha status)
- [X] Added new per system or game custom settings:
    - Aspect Ratio
    - Volume
    - Performance Level
- [X] Added ability to downscale in Pixel Perfect aspect ratio mode when content has more resolution than the screen
- [X] Added libretro SET_MESSAGE and SET_MESSAGE_EXT API implementation (OSD core messages)
- [X] Added menu refresh after option command execution
- [X] Fixed action command executed when option is disabled
- [X] Fixed crash when input.cfg is missing
- [X] Fixed OpenGL bug not properly clearing main FBO making content backgroung to draw garbage in some scenarios

## v0.27.0
- [X] Added game system settings engine and menu options
- [X] Added color highlight to option values for better readability
- [X] Added core name and version to game settings menu
- [X] Added linear interpolation to glcores with vertical resolution >= 480
- [X] Added system options blacklist functionality
- [X] Added system options default configurations for both LCD and CRT functionality
- [X] Added company names to system view for better grouping and sorting
- [X] Added default Roland GM sound font to ScummVM system
- [X] Updated libretro API interface header file
- [X] Changed Home btn so that it always returns to system menu
- [X] Changed `RETRO_ENVIRONMENT_GET_TARGET_REFRESH_RATE` behaviour (fixes ScummVM)
- [X] Changed favs and recent game display names (prettyfied)
- [X] Fixed crash for cores not supporting savestates
- [X] Fixed gl_init on `RETRO_ENVIRONMENT_SET_SYSTEM_AV_INFO` (fixes BLARGG filters)
- [X] Fixed audio gpio dac output selection in audio options (developer purposes)
- [X] Fixed incorrect FBO passed to gl-cores when requesting the same in `RETRO_ENVIRONMENT_SET_HW_RENDER`
- [X] Fixed recents when same roms and different core exists
- [X] Fixed some DC crashes by adding drm_deinit to core_unload_game
- [X] Fixed crash on exit due to duplicated video deinit
- [X] Fixed OpenGL inverted vertical coords after a gl-core game crashes on start
- [X] Fixed name duplication issues in favs and recents (internal company prefix)
- [X] Removed .ipf rom support due to copyright issues

## v0.26.0
- [X] Added MAME 2K3+ system
- [X] Fixed input info display lenght
- [X] Removed SEGA ST from boot to folder option

## v0.25.0
- [X] Added new system menu screen
    - Added new save/load UI system engine
    - Added resume/reset game functionality
- [X] Added system version information in replay optons menu
- [X] Added new default background and system logo
- [X] Updated all cores (compiled on 2023-12-17)

## v0.24.0
- [X] Added boot to system folder option
- [X] Added Philips CD-i system (do not support FMV games)
- [X] Added 3DO system
- [X] Added Atari Lynx system
- [X] Added Nintendo DS system (RPi5)
- [X] Added single monitor option (less performance impact when two monitors are connected)
- [X] Added ability to change audio output device without rebooting the system
- [X] Added ability to remove recents
- [X] Added ability to automatically filter out systems not supporting CRT mode
- [X] Added ability to automatically set default aspect ratio when selecting dual/single monitor mode
- [X] Added player/controller information
- [X] Fixed resolution for cores not honoring `RETRO_ENVIRONMENT_SET_GEOMETRY`
- [X] Fixed deemed extensions in favs and recents
- [X] Fixed recents not working with arcade games
- [X] Fixed libretro log levels
- [X] Fixed crash unloading sound engine when bad rom is loaded
- [X] Fixed UI scaling bug on dual monitor mode

## v0.23.0
- [X] Added Raspberry Pi 3B/3B+/3A+ support
- [X] Added new libretro based configuration engine for system and cores
- [X] Added system info (eth IP, wlan IP and available space)
- [X] Added gamepad test rumble support option
- [X] Added screen position X/Y option for CRT mode
- [X] Added autostart game functionality
- [X] Added Kiosk mode config parameter
- [X] Added option to set Select button for setting favorites
- [X] Added volume configuration to the audio resample engine + volume option
- [X] Added MAME system
- [X] Added self restart capability in case that loading a rom crashes
- [X] Added system option to flter out by vertical and horizontal games
- [X] Added performance level profile option
- [X] Added firstboot time auto configuration based on RPi model
- [X] Added option value info text support
- [X] Added system information
- [X] Changed Python utility to generate arcade title info from FBNeo + MAME full Arcade DAT
- [X] Fixed incorrect Full Native and Integer Scaled aspect ratios on some games
- [X] Fixed bug drawing dimmed files extensions
- [X] Fixed several bugs when saving and displaying arcade games in favorites and recent
- [X] Fixed crash and bug on letter navigation functionality on recents and system folders
- [X] Fixed analog-to-digital option making dpad not working when disabled
- [X] Fixed internal UI view Id state
- [X] Changed default alsa volume levels to 80% (80-100% can cause saturation on some systems)

## v0.22.0
- [X] Added HDMI dual screen support with automatic detection
    - Added duplicated display mode
    - Added side-by-side extended display mode
    - Added vertical stack extended display mode
- [X] Added Raspberry Pi 4/5 model detection
- [X] Fixed UI video corruption after pause

## v0.21.0
- [X] Added pause functionality when UI menu is open
- [X] Added system halt state (P key) for CRT user photos 
- [X] Fixed some UI memory leaks

## v0.20.0
- [X] Added arcade naming database engine
- [X] Added supported file extensions filter
- [X] Added Sega Game Gear in extended view mode
- [X] Added UI text scrolling effect
- [X] Added Python utility to generate arcade title info from FBNeo full Arcade DAT
- [X] Improved UI message engine performance
- [X] Improved configuration engine performance when reading files
- [X] Fixed Atari 2600 horizontal resolution (in replay)
- [X] Fixed Amstrad CPC horizontal resolution (in core)
- [X] Fixed a crash when core incorrectly reports a NULL configuration value
- [X] Fixed UI dimmed font icon chars
- [X] Fixed UI folder elipsis position
- [X] Removed ScummVM core Exit button (not needed)

## v0.19.0
- [X] Changed core neocd by FBNeo (more accurate)
- [X] Changed core mednafen_supergrafx by mednafen_pce (more accurate)
- [X] Fixed UI in 32 bit XRGB8888 pixel format
- [X] Updated all cores (compiled on 2023-09-17)

## v0.18.0
- [X] Added option for selecting the menu hotkey (Home button, Hold Start, and Select + Start combo)
- [X] Added logic to SDL to check if monitor is powered on
- [X] Added video option for helping color blind people (Protanopia, Deuteranopia and Tritanopia)
- [X] Added Dark/Light scanline filters
- [X] Added Recent played games folder
- [X] Changed audio resampler engine to always output at 48000 kHz instead of dynamic native rates
- [X] Fixed HDMI audio handshake in some monitors/TVs
- [X] Fixed favorite foldes sorting

## v0.17.0
- [X] Added Coin-op timer game mode
- [X] Added favorites info message (add/remove)
- [X] Added favorites game launcher functionality

## v0.16.0
- [X] Added new functionality to set proper UI boot menu aspect ratio and resolution

## v0.15.0
- [X] Improved UI performance
- [X] Fixed UI memory leak (items index mismatch)
- [X] Removed unused code (code clean up)

## v0.14.0
- [X] Added new video_show_info option and info message
- [X] Added controller info message
- [X] Added fps counter info message

## v0.13.0
- [X] Added initial information message engine
- [X] Changed UI font to embeded hex compiled code
- [X] Changed UI rotation and activation logic
- [X] Fixed system filter list (read only supported systems)

## v0.12.0
- [X] Added new audio gain engine to avoid clipping artifacts on high freqs
- [X] Added new audio buffer/unpause engine on init
- [X] Added new Full Aspect Ratio scaling mode
- [X] Added system UI swap A/B buttons option
- [X] Added logic to set the controller status to ready only when connected and not buttons are phisically pressed
- [X] Added SN30 Gamepad mapping to game controllers DB
- [X] Added new Favorites engine
- [X] Added default Game Boy Player mode to GBA core (rumble support)
- [X] Added wait state until a monitor is connected on program start
- [X] Added improved debug system levels
- [X] Added basic UI/UX features
    - List menus only loops when using (UP) and (DOWN)
    - Allow going back using both (B) button or (..) special entry
    - Allow back navigation full index history
    - Dimmed file extension color
    - Hide menu when launching game from UI
    - Hide menu when launching game from CLI
- [X] Fixed crashes on several cores where log info introduces bad chars
- [X] Fixed Keyboard fallback game controller
- [X] Fixed menu not displayed with home button afer rotating
- [X] Fixed DC crash when unloading core
- [X] Fixed N64 crash when unloading core
- [X] Fixed verbose DEBUG mode not working fine on non ssh session
- [X] Fixed N64 game launcher crash
- [X] Fixed DC game launcher crash
- [X] Fixed SNES game launcher crash
- [X] Fixed FBNEO game launcher crash
- [X] Fixed N64 bad textures when launched from UI
- [X] Fixed DC bad textures when launched from UI
- [X] Fixed standalone game launcher
- [X] Fixed save/load functions
- [X] Fixed no HDMI sound when launching games from UI
- [X] Fixed audio stuttering for some games on load
- [X] Fixed gamepad not working on PSX games when launched from UI

## v0.11.0
- [X] Added new audio engine
    - Based on Dynamyc Rate Control
    - Based on SINC resampling algorithm
    - Low latency and CPU ussage

## v0.10.0
- [X] Added initial UI engine
    - Integer scale
    - Rotation +/-90
    - Auto scaling factor
- [X] Added 4 players support
- [X] Added controller sorting engine
    - Player number assigned by connection order
    - Connected controllers keep player number
    - New controllers take first free player number
- [X] Added new input configuration file
- [X] Added controller rumble implementation
- [X] Added input descriptors implementation
- [X] Added controller info implementation
- [X] Added support for 0RGB1555, XRGB8888 and RGB565 pixel formats

## v0.9.0
- [X] Added dynamic rate control for Atomis/Naomi/DC games running at 60/30 fps
- [X] Added core assets directory implementation
- [X] Added disk control interface version implementation
- [X] Fixed cores that request OpenGL ES 3.0 context instead of 3.1

## v0.8.0
- [X] Added a/v sync to content engine (i.e. run PAL games nicely)
- [X] Added headphone/hdmi audio output selector
- [X] Fixed crash when unloading games using core threading

## v0.7.0
- [X] Added custom input poll for cores not honoring libretro input poll callback
- [X] Added new option to display FPS
- [X] Fixed PSX support
- [X] Fixed all libretro-gl core performance issues
- [X] Fixed crash when booting with monitor powered off
- [X] Fixed crash when saving SRAM on some games
- [X] Fixed screenshot crashes in some cores
- [X] Fixed savestate crashes in some cores
- [X] Fixed SRAM crashes in some cores

## v0.6.0
- [X] Added video scalling configurations (Full 4:3, Native 1:1, Integer Scaled HV)
- [X] Added user screenshot functionality (F10)
- [X] Added system screenshot functionality (on savestates)
- [X] Fixed several bugs in the configuration file engine

## v0.5.0
- [X] Added system option to enable/disable verbosity
- [X] Added load/save system and core configuration file support
- [X] Added DragonRise controller mappings
- [X] Added user savestates support (F5/F9)
- [X] Added support for .zip files (only supported cores)
- [X] Fixed crash when pressig keyboard arrows with a controller connected
- [X] Fixed keyboard/controller priority when connected and/or disconnected

## v0.4.0
- [X] Added support for native SRAM save files
- [X] Added initial support for libretro-gl cores

## v0.3.0
- [X] Added basic system configuration file engine
- [X] Added automatic core identification
- [X] Added new input engine with controller DB
- [X] Added analog to digital input option

## v0.2.0
- [X] Added automatic monitor EDID video selector (best mode)
- [X] Added new audio sync engine
    - Low latency
    - Prevents buffer underrun and overrun
    - Adaptative speed to video refresh rate

## v0.1.0
- [X] Added support for Raspberry Pi 4 using KMS/DRM, EGL, GBM and OpenGL ES 3.X
- [X] Added basic support for audio and input via SDL2
- [X] Added basic support for non-libretro-gl cores