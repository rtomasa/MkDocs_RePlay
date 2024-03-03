Here are some Frequently Asked Questions that people often have:

## Does it work on PC?
No, it doesn't, and probably never will. RePlay is developed with many features relying on ARM architecture and Raspberry Pi devices.

## Does it work on other devices like Orange Pi?
No, it doesn't, and never will. Other devices completely lack support for Linux OpenGL ES in KMS/DRM video mode (no X), among other things. Another important missing feature on any other device, besides Raspberry Pi, is the lack of DPI (Display Parallel Interface), which is required for CRT TV support.

## What is the advantage over other RPi distros like Lakka, RetroPie, or RecalBox?
Since the system is entirely focused on a single device family with a limited list of supported systems, I can maximize the hardware's power and introduce many unique features. It's also worth noting that the system is extremely fast and user-friendly, with each system core thoroughly tested and pre-configured. This ensures the best experience right out of the box.

## Why RePlay OS instead of a new RGB-Pi OS 5?
The primary aim of RePlay OS is to offer a system that is fast and easy to start with. It demonstrates that emulation can achieve high quality when properly configured, allowing everyone to enjoy optimal gaming conditions from the start, without requiring technical emulation skills to fine-tune everything.

In all versions of RGB-Pi OS (0, 1, 2, 4), we were limited by the two frontends used—mine for the user interface and RetroArch for gaming. This limitation prevented certain functionalities, such as in-game menu rotation, a fully adaptable interface across various resolutions, customization based on my design preferences, and more.

RePlay's frontend is not just a simple launcher; it is a complete libretro-based frontend similar to the one utilized in RetroArch/Lakka.

Numerous features are exclusively achievable by using a custom libretro-based frontend, which cannot be accomplished using a basic launcher paired with RetroArch. These include dual-screen support, minimal input lag—comparable to or even less than that of the original hardware without utilizing runahead—complete control over various system options and configurations, core speed and performance enhancements, improvements in DynaRes engine speed for CRT TVs, special functionalities like the coin-op time feature, and many others.

It's crucial to note that RePlay is compatible with both LCD and CRT monitors, and it will support other ongoing RGB-Pi projects.

## What about input lag?
The system runs by default in a super low-latency mode, adding only 0/1 frame of lag over the real system hardware.

Looking for more? RePlay also includes a performance system option where you can select a profile to achieve the same or even less input lag than real hardware. This mode avoids the use of advanced and complex features like runahead, ensuring 100% compatibility with every emulated system. However, it requires a fairly powerful CPU and GPU, so not all systems run well on all Raspberry Pi models.

Also, please note that some system cores provide their own custom runahead functionality. When combined with this feature, input lag could be significantly less than that experienced on the real hardware.

## Is it OpenSource?
No, it isn't. It is freeware, but maybe I'll open source it in the future.

Since this is a full-time job in my spare time, I like to have full control of the project and avoid any kind of forking at the moment to prevent me from losing interest in the development.

## Can you add feature X to RePlay?
The answer is likely to be no, as I'm trying to keep the system easy and small from both user and developer perspectives.

## Is there any deadline for the first release?
No, there isn't. It will be released when it is finished.

## Will it be compatible with CRT TVs and RGB-Pi or other devices?
The system is being developed using RGB-Pi hardware, and no other devices will be supported or tested.

Initially, only Raspberry Pi 4 and 5 will support CRT TVs. RPi 3 and Zero 2 are still pending on feasibility.

**Note about Pi5 support:** we already tested video DPI compatibility with current hardware. Sound is still pending on further analysis and official Raspberry drivers.

## Will it support image scrapping?
No, it won't. The main goal of the system is to be super fast with zero configuration. This means that no scanning or database is used by the system, so scrapping is not even feasible from a technical point of view. Additionally, the UI layout makes it impossible to fit images on either LCD or CRT screens.

## Can I use other cores?

The answer is no. All the cores included in RePlay have been selected based on a balance between the best performance and emulation quality across different supported models of Raspberry Pi. That being said, depending on each Raspberry Pi model, some systems may be activated or deactivated, and it's possible that cores within the same system may also be changed. All the cores have been tested for years and come with optimal default configurations based on performance, emulation quality, fidelity, bugs, screen type, etc.

## What is libretro?

The Libretro API is a lightweight C-based Application Programming Interface (API) that exposes generic audio, video, and input callbacks.

There are two sides to Libretro development:

- **frontends** are programs that provide a user interface and all the implementation-specific details to run libretro-compatible cores.
- **cores** are programs built as a single library file (such as a game, emulator, or media player) that use the libretro API so that can be executed by libretro frontends.

Developers of cores don’t have to worry about writing different video drivers for Direct3D, OpenGL or worrying about catering to all possible input APIs, sound APIs, gamepads, etc.

**RePlay OS** uses a custom libretro frontend specifically tailored to Raspberry devices. It is programmed in C and uses the following libraries:

- OpenGL ES 3.X for video
- SDL2 for audio and input devices

## Can I use CRT shaders on my LCD?

No, that's not possible. The system offers only two basic scanline shaders tailored for LCD screens, and they're activated exclusively when integer scaling is enabled. These shaders are intended to provide a subtle texturing effect for those who prefer it, rather than to simulate the appearance of a CRT screen.

Attempting to replicate the authentic CRT TV experience using CRT shaders is beyond the project's intended scope and philosophy. In fact, CRT shaders introduce image aberrations and performance issues that vary depending on the system in use. Additionally, they cannot reproduce the distinctive contrast or smooth motion of a real CRT TV.

If you're fond of the look and feel of CRT TVs, your best bet is to acquire an actual CRT TV!