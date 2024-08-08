# Changelog

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
<!-- **IMPORTANT!!! This is the last version containing development code for old RGB-Pi standard A/V** -->
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
    - Integer Scale Underscan (usefull for special DIY projects)
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
- [X] Fixed core crashes due to a bug in RETRO_ENVIRONMENT_SET_MESSAGE
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
- [X] Changed RETRO_ENVIRONMENT_GET_TARGET_REFRESH_RATE behaviour (fixes ScummVM)
- [X] Changed favs and recent game display names (prettyfied)
- [X] Fixed crash for cores not supporting savestates
- [X] Fixed gl_init on RETRO_ENVIRONMENT_SET_SYSTEM_AV_INFO (fixes BLARGG filters)
- [X] Fixed audio gpio dac output selection in audio options (developer purposes)
- [X] Fixed incorrect FBO passed to gl-cores when requesting the same in RETRO_ENVIRONMENT_SET_HW_RENDER
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
- [X] Fixed resolution for cores not honoring RETRO_ENVIRONMENT_SET_GEOMETRY
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