Here are some Frequently Asked Questions that people have.

## Does it work on PC?
No it doesn't, and never will. RePlay is developed with many features relying on ARM architecture and Raspberry Pi devices.

## Does it work on other devices like Orange Pi?
Again no, and never will. Other devices fully lack the support for linux video drivers and OpenGL ES in KMS video mode (no X) among other things. Another important missing feature of any other device other than Raspberry Pi, is the lack of DPI (Display Parallel Interface) wich is required for CRT TV support.

## What is the advantage over other RPi distros like Lakka, RetroPie or RecalBox?
Since the system is fully focused on a single device family with a limited list of supported systems, I can maximize the hardware's power and introduce many unique features. It is also worth noting that the system is extremely fast and user-friendly, with each system core thoroughly tested and pre-configured. This ensures the best experience right out of the box.

## Why RePlay OS instead of a new RGB-Pi OS 5?

The primary aim of RePlay OS is to offer a system that is fast and easy to start with. It demonstrates that emulation can achieve high quality when properly configured, allowing everyone to enjoy optimal gaming conditions right from the start, without requiring technical emulation skills to fine-tune everything.

In all versions of RGB-Pi OS (0, 1, 2, 4), we were limited by the two frontends used—mine for the user interface and RetroArch for gaming. This limitation prevented certain functionalities, such as in-game menu rotation, a fully adaptable interface across various resolutions, customization based on my design preferences, and more.

RePlay's frontend is not just a simple launcher; it is a complete libretro-based frontend similar to the one utilized in RetroArch/Lakka.

Numerous features are exclusively achievable by using a custom libretro-based frontend, which cannot be accomplished using a basic launcher paired with RetroArch. These include dual-screen support, minimal input lag—comparable to or even less than that of the original hardware without utilizing runahead—complete control over various system options and configurations, core speed and performance enhancements, improvements in DynaRes engine speed for CRT TVs, special functionalities like the coin-op time feature, and many others.

It's crucial to note that RePlay is compatible with both LCD and CRT monitors, and it will support our ongoing projects.

## What about input lag?
The system runs by default in a super low-latency mode, adding only 0/1 frame of lag over the actual system hardware.

Looking for more? RePlay also includes a performance system option where you can select a profile to achieve the same or even less input lag than real hardware. This mode avoids the use of advanced and complex features like runahead, ensuring 100% compatibility with every emulated system. However, it requires a fairly powerful CPU and GPU, so not all systems run well on all Raspberry Pi models.

## Is it OpenSource?
No it isn't. It is Freeware, but maybe I'll be open the same in the future.

Since this is a full time job in my spare time, I like to have full control of the project and avoid any kind of forking by the moment to prevent me from loosing interest on the development.

## Can you add feature X to RePlay?
The answer is likely to be no, as I'm trying to keep the system easy and small from both user and developer perspectives.

## Is there any deadline for the first release?
No it isn't. It will be released when it is finished.

## Will it be compatible with CRT TVs and RGB-Pi or other devices?
The system is being developed using RGB-Pi hardware and no other devices will be supported or tested.

Initially only Raspberry Pi 4 and 5 will support CRT TVs. RPi 3 is still pending on feasibility.

**Note about Pi5 support:** we already tested video DPI compatibility with current hardware. Sound is still pending on further analysis and official Raspberry drivers.

## Will support image srapping?
No it won't. The main goal of the system is to be super fast with zero configuration. This means that no scanning or database is used by the system so scrapping is not even feasible from the technical point of view. Also the UI layout makes impossible to fit images neither on LCD or CRT screens.