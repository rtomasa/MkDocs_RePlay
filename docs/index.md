---
template: home.html
hide:
  - path
---

<figure class="home-logo" markdown>
  ![RePlayOS Logo](img/banner.png){width="500"}
</figure>

<div class="video-grid">
  <div class="video video--portrait">
    <iframe
      src="https://www.youtube.com/embed/3kO8zVI4iKE?si=vQNc7IlAG013Oskz&amp;controls=0"
      title="PuncOut!!"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      referrerpolicy="strict-origin-when-cross-origin"
      allowfullscreen>
    </iframe>
  </div>

  <div class="video video--portrait">
    <iframe
      src="https://www.youtube.com/embed/Ld8jyQTJ8WM?si=YKffZgaeZcStcxac&amp;controls=0"
      title="Dead or Alive 2"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      referrerpolicy="strict-origin-when-cross-origin"
      allowfullscreen>
    </iframe>
  </div>

  <div class="video video--portrait">
    <iframe
      src="https://www.youtube.com/embed/_avTwSmXQfk?si=b73j5qyM2nWeYyrf&amp;controls=0"
      title="Time Crisis"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      referrerpolicy="strict-origin-when-cross-origin"
      allowfullscreen>
    </iframe>
  </div>

  <div class="video video--portrait">
    <iframe
      src="https://www.youtube.com/embed/KBUWhvnCt3U?si=WVkozFkys9KcU_Mo&amp;controls=0"
      title="Radiant Silvergun"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      referrerpolicy="strict-origin-when-cross-origin"
      allowfullscreen>
    </iframe>
  </div>
</div>

<div class="patreon-button" markdown>
  [Join my Patreon :simple-patreon:](https://patreon.com/RePlayOS){ .md-button target=_blank }
</div>

## What is RePlayOS?

**RePlayOS** is a Linux distribution featuring a streamlined [libretro](./faq.md/#what-is-libretro) frontend. It's specifically designed to emulate a wide range of classic game consoles, arcade machines, and computers. The OS focuses on delivering a fast and user-friendly emulation experience, optimized for use with Raspberry Pi boards in both LCD and CRT screens.

Have more questions? Please check the [F.A.Q](./faq.md) section for further information.

## Meet Replay Control

**Your RePlayOS library, in your hand.** Replay Control is the companion web app for RePlayOS. Use your phone, tablet, or computer to browse your game library, launch games on the TV, manage favorites, and configure your system over your local network.

Replay Control was created by [Antonio Abad (lapastillaroja)](https://github.com/lapastillaroja){ target=_blank rel="noopener" }.

<div class="companion-showcase">
  <div class="video">
    <iframe
      src="https://www.youtube.com/embed/jUIY4TUs3KE?si=gSX_hIrhXsY634fw"
      title="Replay Control showcase"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      referrerpolicy="strict-origin-when-cross-origin"
      loading="lazy"
      allowfullscreen>
    </iframe>
  </div>
</div>

<div class="companion-actions" markdown>
  [Learn about Replay Control](replaycontrol.md){ .md-button .md-button--primary }
  [Visit the Replay Control website](https://lapastillaroja.github.io/replay-control/){ .md-button target=_blank rel="noopener" }
</div>

## Main Features

- Support for [Raspberry Pi with 64-bit CPU models](./sysreq.md), KMS/DRM and OpenGL ES (with compatibility paths for older Pi models).
- Automatic detection of Raspberry Pi model. Same system (SD card) can be used in any supported model.
- Support for both GL and Non-GL libretro based cores.
- Support for both LCD and CRT screens via [DynaRes 2.0](index.md#dynares-20) engine.
- Support for single or dual screen configurations in both LCD and CRT modes.
- Low latency video engine (comparable to real hardware not using runahead).
- Low latency audio resampler engine (32ms average).
- Low latency input engine (can check all button status in one single read per frame).
- Support for easy virtual disk engine.
- Out of the box automatic core configuration based on Pi model, emulated system, and monitor type.
- Out of the box support for more than 700 game controllers.
- Support for audio normalization.
- Support for external USB/GPIO audio DACs.
- Support for [RetroAchievements](rcheevos.md) in compatible libretro cores and games.
- Experimental [Insider Replays](replays.md) input recording and playback for compatible cores.
- Experimental Vulkan renderer on Raspberry Pi 5 for authenticated Insiders; OpenGL ES remains the default.
- Experimental GameCube, Wii, Triforce, and PlayStation 2 cores on Insider Pi 5 systems using Vulkan; Virtual Boy is available on all supported Pi models.
- Balanced and low-latency frame pacing options globally and per game.
- [Replay Control](replaycontrol.md) companion web app for browsing, managing, and launching games from another device.
- Support for [Link Play](linkplay.md) core-managed multiplayer over a local network.
- Signed, transactional [software updates](updates.md) with stable and testing channels.
- Play statistics for current games, sessions, weeks, and lifetime usage.
- Separate data-location control for shared ROM libraries and local saves/settings.
- Adaptative frontend UI integer scaling, based on system resolution.
- Support for multiple screen rotation modes for both UI and system/games.
- Support for six players.
- Support for Favorites and Recent played game list.
- Support for Coin-op timer game mode.
- Internal arcade game data base for properly displaying game names in frontend UI.
- Support for a system halt state (using H key) to facilitate people taking photos of CRT screens.
- Support for user X/Y screen position adjustment, gamma and RGB color correction in both LCD and CRT modes.
- Support for Kiosk mode.
- Support for [autostart games](autostart.md) on system boot for real arcade cabinet experience.
- Support for real GunCon2 lightgun in CRT TVs via custom driver and frontend special functionalities.
- Support for RPi5 RetroFlag cases
- Ability to filter out arcade games by number of players, number of screens, number of buttons, and screen orientation.
- Ability to filter out by arcade, consoles, computers, and handhelds
- Ability to boot right into specific system folder for better experience on custom builds.
- Ability to enable dynamic colored borders via the AmbiScan feature.
- Support for setting the RGB color range (full or limited) for external video DACs.

## DynaRes 2.0

When RePlayOS is executed on a CRT TV, CRT PC monitor, or CRT Arcade screen, it makes use of the **DynaRes** engine which provides the following advanced features:

- **Native Timings**: games are displayed using native horizontal and vertical resolutions and refresh rates.
- **On-The-Fly Timing Changes**: the system is able to make instant timing changes for games that use different resolutions during the gameplay.
- **Calamity Modeline Calculator**: for modeline calculations, DynaRes takes advantage of Calamity's switchres dynamic library for calculating all system modelines.
- **Interlaced Flicker Reduction**ː the system automatically applies a linear filter for smoothing the flickering produced in games that use interlaced video modes (slightly reducing the image sharpness).
- **Software X/Y Position**: it is possible to adjust the screen X/Y position via software menu option (no forced modelines).
- **CRT Profiles**: the modelines generated by the system can be configured to better adjust to different CRT types like consumer TVs, PC 31kHz monitors, Arcade 15, 25 and 31kHz, etc.
- **Dual Screen**: you can choose from three different dual screen configurations: cloned image, side-by-side, and stacked monitors.
- **CSYNC Mode Selector**: you can choose different video signal mixer modes: Separated H/V, Csync (AND), Csync (XOR).

DynaRes can also operate in GRR (**Game Refresh Rate**) mode on LCD screens, using the refresh rate reported by the running game when available. This is distinct from VRR and works on supported displays.

*Note: Dual Screen is also available when LCD mode is set.*

## Custom Cores

RePlayOS provides several utility cores out of the box:

- **PiBench**: a software render core for measuring Raspberry Pi CPU performance.
- **Screen Test**: a simple core for checking CRT geometry and color range, with support for both NTSC and PAL modes (60/50Hz)
- [Alpha Player](alphaplayer.md): a custom media player for playing video and audio files, with support for many formats.
