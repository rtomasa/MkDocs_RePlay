# Features

## Libretro Based Frontend

RePlay OS is based on [![Libretro Logo](img/libretro.png){width="150"; align=top}](https://www.libretro.com/index.php/api/) API for implementing the frontend and executing the different core emulators.

Libretro is a lightweight C-based Application Programming Interface (API) that exposes generic audio, video, and input callbacks.

There are two sides to Libretro development:

- **frontends** are programs that provide a user interface and all the implementation-specific details to run libretro-compatible cores.
- **cores** are programs built as a single library file (such as a game, emulator, or media player) that utilize the libretro API, enabling execution by libretro frontends.

Core developers don't need to write different video drivers for Direct3D, OpenGL, or cater to various input APIs, sound APIs, gamepads, etc.

## Main Features

- Support for Raspberry Pi 3/4/5 using 64bit Linux, KMS/DRM and OpenGL ES 3.X (OpenGL ES compatibility mode in Pi3 models).
- Automatic detection of Raspberry Pi model. Same system (SD card) can be used in any supported model.
- Support for both GL and Non-GL libretro based cores.
- Support for both LCD and CRT screens via [DynaRes 2.0](features.md#dynares-20) engine.
- Support for single or dual screen configurations in both LCD and CRT modes.
- Support for different performance profiles.
- Support for non-runahead Zero lag mode, fully compatible with all systems and games (requires fairly powerfull CPU for properly work on certain systems and games).
- Support for easy virtual disk engine.
- Out of the box automatic core configuration based on Pi model, emulated system, and monitor type.
- Out of the box support for more than 700 game controllers.
- Low latency audio resampler engine.
- Adaptative frontend UI integer scaling, based on system resolution.
- Support for frontend UI rotation independently of the running system/game (90, 180 and 270 degrees).
- Support for six players.
- Support for Favorites and Recent played game list.
- Support for Coin-op timer game mode.
- Internal arcade game data base for properly displaying game names in frontend UI.
- Support for a system halt state (using P key) to facilitate people taking photos of CRT screens.
- Support for user X/Y screen position adjustment in both LCD and CRT modes.
- Support for Kiosk mode.
- Support for autostart games on system boot for real arcade cabinet experience.
- Ability to filter out arcade games by screen type (horizontal, vertical, dual sisde-by-side, and vertical stack).
- Ability to boot right into specific system folder for better experience on custom builds.

## DynaRes 2.0

When RePlay OS is executed on a CRT TV or CRT Arcade monitor, RePlay makes use of the **DynaRes** ![DynaRes Logo](img/dynares.png){align=top} engine which provides the following advanced features:

- **Native Timings**: games are displayed using native horizontal and vertical resolutions and refresh rates.
- **On-The-Fly Timing Changes**: the system is able to make instant timing changes for games that use different resolutions during the gameplay.
- **Calamity Modeline Calculator**: for modeline calculations, DynaRes takes advantage of Calamity's switchres dynamic library for calculating all system modelines.
- **Interlaced Flicker Reduction**ː the system automatically applies a linear filter for smoothing the flickering produced in games that use interlaced video modes (slightly reducing the image sharpness).
- **Software X/Y Position**: it is possible to adjust the screen X/Y position via software menu option (no forced modelines).
- **CRT Profiles**: the modelines generated by the system can be configured to better adjust to different CRT types like consumer TVs, Arcade 15, 25 and 31Khz, etc.
- **Improved Overscan**: it allows you to choose between native or improved image overscan, providing additional horizontal view area that is typically hidden.
- **Dual Screen**: you can choose from three different dual screen configurations: cloned image, side-by-side, and stacked monitors.

*Note: Dual Screen is also available when LCD mode is set.*