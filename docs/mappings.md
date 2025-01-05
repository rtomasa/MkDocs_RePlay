# New Controllers Support

RePlay OS comes with a predefined controller database, allowing your gamepad and joysticks to work out of the box. This support is based on the [SDL_GameControllerDB](https://github.com/mdqinc/SDL_GameControllerDB){target=_blank} project, which currently supports more than **630** different controllers and revisions right out of the box.

If your gamepad or joystick is not detected when connected to RePlay OS, you can still create a new SDL controller mapping by following the instructions provided in the official GitHub repository.

You have two options: you can fork the project and contribute by submitting your own mappings following the SDL standard Xinput/Hori mapping layout, or you can create a new one based on the instructions below and send it to me, and I'll prepare the same on your behalf.

Please note that when following the instructions for creating the mapping, if you create it on a Windows or macOS, the mapping may differ from one created in a Linux environment, which could result in a non-working mapping in RePlay OS. For this reason, I strongly recommend following these steps:

1. Create the new mapping. Two options here:
    * **Forking and contributing to the official SDL DB**. Create the new controller mapping by following the instructions in the [SDL_GameControllerDB](https://github.com/mdqinc/SDL_GameControllerDB){target=_blank} GitHub repository.
    * **Creating the mapping specifically for RePlay OS**. Use the same instructions like above but use the below [Mapping Guide](#mapping-guide) instead.
2. If the mapping was created on a system other than Linux, please update your mapping by replacing the platform parameter with the Linux value.
3. Copy your new mapping to `<unit>/config/input/sdlusermapsdb.txt` system file. This file could be in the SD or USB unit depending on whether you are using the SD or USB external unit.
4. Reboot the system.
5. Check if the controller works.
6. If it works, submit a Pull Request to the GitHub repository or send the mapping to me.

## Mapping Guide

We strongly suggest following the next maping guide when creating a new mapping for RePlay OS:

![Mapping GUide](img/mapping_guide.png)