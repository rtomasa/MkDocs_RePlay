# Home

<figure markdown>
  ![Anime Girl](img/bg.png)
</figure>

<figure markdown>
  ![RePlay OS Logo](img/banner.png){width="500"}
  <br>
  [Join my Patreon :simple-patreon:](https://patreon.com/RePlayOS){ .md-button target=_blank }
</figure>

## What is RePlay OS?

**RePlay OS** is a Linux distribution featuring a streamlined [libretro](./faq.md/#what-is-libretro) frontend. It's specifically designed to emulate a wide range of classic game consoles, arcade machines, and computers. The OS focuses on delivering a fast and user-friendly emulation experience, optimized for use with Raspberry Pi boards in both LCD and CRT screens.

Have more questions? Please check the [F.A.Q](./faq.md) section for further information.

## Main Features

- Support for [Raspberry Pi with 64bit CPU models](./sysreq.md), KMS/DRM and OpenGL ES 3.X (OpenGL ES compatibility mode in Pi3 and Zero 2 models).
- Automatic detection of Raspberry Pi model. Same system (SD card) can be used in any supported model.
- Support for both GL and Non-GL libretro based cores.
- Support for both LCD and CRT screens via [DynaRes 2.0](index.md#dynares-20) engine.
- Support for single or dual screen configurations in both LCD and CRT modes.
- Support for different performance profiles.
- Support for non-runahead Zero lag mode, fully compatible with all systems and games.
- Support for easy virtual disk engine.
- Out of the box automatic core configuration based on Pi model, emulated system, and monitor type.
- Out of the box support for more than 700 game controllers.
- Low latency audio resampler engine.
- Support for audio normalization.
- SUpport for external USB/GPIO audio DACs.
- Adaptative frontend UI integer scaling, based on system resolution.
- Support for frontend UI rotation independently of the running system/game (90, 180 and 270 degrees).
- Support for six players.
- Support for Favorites and Recent played game list.
- Support for Coin-op timer game mode.
- Internal arcade game data base for properly displaying game names in frontend UI.
- Support for a system halt state (using H key) to facilitate people taking photos of CRT screens.
- Support for user X/Y screen position adjustment, gamma and RGB color correction in both LCD and CRT modes.
- Support for Kiosk mode.
- Support for autostart games on system boot for real arcade cabinet experience.
- Support for real GunCon2 lightgun in CRT TVs via custom driver and frontend special functionalities.
- Support for RPi5 RetroFlag cases
- Ability to filter out arcade games by number of players, number of screens, number of buttons, and screen orientation.
- Ability to filter out by arcade, consoles, computers, and handhelds
- Ability to boot right into specific system folder for better experience on custom builds.
- Ability to enable dynamic colored borders via the AmbiScan feature.
- Support for setting the RGB color range (full or limited) for external video DACs.

## DynaRes 2.0

When RePlay OS is executed on a CRT TV, CRT PC monitor, or CRT Arcade screen, it makes use of the **DynaRes** engine which provides the following advanced features:

- **Native Timings**: games are displayed using native horizontal and vertical resolutions and refresh rates.
- **On-The-Fly Timing Changes**: the system is able to make instant timing changes for games that use different resolutions during the gameplay.
- **Calamity Modeline Calculator**: for modeline calculations, DynaRes takes advantage of Calamity's switchres dynamic library for calculating all system modelines.
- **Interlaced Flicker Reduction**ː the system automatically applies a linear filter for smoothing the flickering produced in games that use interlaced video modes (slightly reducing the image sharpness).
- **Software X/Y Position**: it is possible to adjust the screen X/Y position via software menu option (no forced modelines).
- **CRT Profiles**: the modelines generated by the system can be configured to better adjust to different CRT types like consumer TVs, PC 31kHz monitors, Arcade 15, 25 and 31kHz, etc.
- **Improved Overscan**: it allows you to choose between native or improved image overscan, providing additional horizontal view area that is typically hidden.
- **Dual Screen**: you can choose from three different dual screen configurations: cloned image, side-by-side, and stacked monitors.
- **CSYNC Mode Selector**: you can choose different video signal mixer modes: Separated H/V, Csync (AND), Csync (XOR).

*Note: Dual Screen is also available when LCD mode is set.*

## Custom Cores

RePLay OS provides several utility cores out of the box:

- **PiBench**: a software render core for measuring Raspberry Pi CPU performance.
- **Screen Test**: a simple core for checking CRT geometry and color range, with support for both NTSC and PAL modes (60/50Hz)
- [Alpha Player](alphaplayer.md): a custom media player for playing video and audio files, with support for many formats.