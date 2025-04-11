Here are some Frequently Asked Questions that people often have:

## Does it work on PC?
No, it doesn't, and probably never will. RePlay is developed with many features relying on ARM architecture and Raspberry Pi devices.

## Does it work on other devices like Orange Pi?
No, it doesn't, and never will. Other devices completely lack support for Linux OpenGL ES and/or KMS/DRM video mode (no X), among other things. 

## What is the advantage over other RPi distros like Lakka, RetroPie, or RecalBox?
Since the system is entirely focused on a single device family with a limited list of supported systems, I can maximize the hardware's power and introduce many [unique features](index.md#main-features). It's also worth noting that the system is extremely fast and user-friendly, with each system core thoroughly tested and pre-configured. This ensures the best experience right out of the box.

## Why RePlay OS instead of a new RGB-Pi OS 5?
The primary aim of RePlay OS is to offer a system that is fast and easy to start with. It demonstrates that emulation can achieve high quality when properly configured, allowing everyone to enjoy optimal gaming conditions from the start, without requiring technical emulation skills to fine-tune everything.

In all versions of RGB-Pi OS (0, 1, 2, 4), we were limited by the two frontends used (mine for the user interface, and RetroArch for gaming). This limitation prevented certain functionalities, such as in-game menu rotation, a fully adaptable interface across various resolutions and devices, customization based on my design preferences, and more.

RePlay's frontend is not just a simple launcher; it is a complete libretro-based frontend similar to the one utilized in RetroArch/Lakka.

Numerous features are exclusively achievable by using a custom libretro-based frontend, which cannot be accomplished using a stand-alone launcher paired with RetroArch. These include dual-screen support, minimal input lag (comparable to or even less than that of the original hardware) without utilizing runahead, complete control over various system options and configurations, core speed and performance enhancements, improvements in DynaRes engine for instant timing changes in CRT TVs, special functionalities like the coin-op time feature, and many others.

It's crucial to note that RePlay is compatible with both LCD and CRT monitors, and it will support future ongoing RGB-Pi projects.

## What about input lag?
By default, the system operates in an ultra-low-latency mode, achieving a remarkable 0 to 1 frame of input lag.

Looking for even more precision? A dedicated latency mode option lets you experience input lag comparable to, or even lower than, real hardware. This mode prioritizes speed by bypassing advanced features like runahead, guaranteeing 100% compatibility across all emulated systems. However, it demands more CPU resources, so feel free to experiment with it in your favorite games and systems to find the perfect balance.

Also, please note that some system cores provide their own custom runahead functionality. When combined with this feature, input lag could be significantly less than that experienced on the real hardware.

## Is it OpenSource?
The OS operates under a dual-license model: while most components are free and open-source, the frontend remains proprietary. For more details, please refer to the licensing information on the [download](download.md#license) page.

## Can you add feature X to RePlay?
The answer is likely to be no, as I'm trying to keep the system easy and small from both user and developer perspectives.

## Is there any deadline for the first release?
No, there isn't. It will be released when it is finished.

## Will it be compatible with CRT TVs and RGB-Pi or other devices?
The system is being developed using new RGB-Pi 2 prototype hardware (new hardware will be announced in the comming months), and no other devices will be supported or tested.

All Raspberry Pi Zero 2, 3, 4 and 5 models will support CRT TVs using both progressive and interlaced video modes.

Other CTR screens like Arcade and PC 31kHz monitors are also supported.

**Note about DPI (GPIO) A/V support:** DPI is not longer compatible with current hardware due to the lack of audio and interlaced video support, so GPIO A/V hardware solutions like vga666 or current RGB-Pi (cable and JAMMA) won't be supported anymore in RePlay OS.

**UPDATE:** Although interlaced support has been reintroduced in the Pi5 through the RP1 chip, its image quality and stability still fall significantly short compared to our new solution..

## Will it support image scraping?
No, it won't. The main goal of the system is to be super fast, easy, and easy to setup. Scraping does not comply with this goal. In addition, it is not even feasible from a technical point of view since the UI layout makes not possible to fit images on either LCD or CRT screens.

## Can I use other cores?

The answer is no. All the cores included in RePlay have been selected and pre-configured based on a balance between the best performance and emulation quality across different supported models of Raspberry Pi. That being said, depending on each Raspberry Pi model, some systems may be activated or deactivated, and it's possible that cores within the same system may also be changed. All the cores have been tested for years and come with optimal default configurations based on performance, emulation quality, fidelity, bugs, screen type, and more.

## What is libretro?

The [Libretro API](https://www.libretro.com/index.php/api/){target=_blank} is a lightweight C-based Application Programming Interface (API) that exposes generic audio, video, and input callbacks.

There are two sides to Libretro development:

- **frontends** are programs that provide a user interface and all the implementation-specific details to run libretro-compatible cores.
- **cores** are programs built as a single library file (such as a game, emulator, or media player) that use the libretro API so that can be executed by libretro frontends.

Developers of cores don’t have to worry about writing different video drivers for Direct3D, OpenGL or worrying about catering to all possible input APIs, sound APIs, gamepads, etc.

**RePlay OS** uses a custom libretro frontend specifically tailored to Raspberry devices. It is programmed in C and uses the following libraries:

- DRM, EGL, and OpenGL ES 3.X for video
- SDL2 for audio and input devices

## Can I use CRT shaders on my LCD?

No, that's not possible. The system offers several scanline shaders tailored for LCD screens and 31kKz CRT monitors, and they're activated exclusively when integer scaling is enabled. These shaders are intended to provide a subtle texturing effect for those who prefer it, rather than to simulate the appearance of a CRT screen.

Attempting to replicate the authentic CRT TV experience using CRT shaders is beyond the project's intended scope and philosophy. In fact, CRT shaders introduce image aberrations and performance issues that vary depending on the system in use. Additionally, they cannot reproduce the distinctive contrast or smooth motion of a real CRT TV.

If you're fond of the look and feel of CRT TVs, your best bet is to acquire an actual CRT TV!
