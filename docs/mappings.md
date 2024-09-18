# New Controllers Support

RePlay OS comes with a predefined controller database, allowing your gamepad and joysticks to work out of the box. This support is based on the [SDL_GameControllerDB](https://github.com/mdqinc/SDL_GameControllerDB){target=_blank} project, which currently supports more than **630** different controllers and revisions right out of the box.

If your gamepad or joystick is not detected when connected to RePlay OS, you can still create a new SDL controller mapping by following the instructions provided in the official GitHub repository.

You have two options: you can fork the project and contribute by submitting your own mappings, or you can send them to me, and I will upload them on your behalf.

Please note that when following the instructions for creating the mapping, if you create it on a Windows or macOS machine, the mapping may differ from one created in a Linux environment, which could result in a non-working mapping in RePlay OS. For this reason, I strongly recommend following these steps:

1. Create the new controller mapping by following the instructions in the [SDL_GameControllerDB](https://github.com/mdqinc/SDL_GameControllerDB){target=_blank} GitHub repository.
2. If the mapping was created on a system other than Linux, please update your mapping by replacing the platform parameter with the Linux value.
3. Copy your new mapping to the very end of the `/opt/replay/data/gamecontrollerdb.txt` system file. Instructions for accessing the file system can be found in the [Adding Games](addgames.md#transfer-roms-over-the-network-via-sftp) section.
4. Reboot the system.
5. Check if the controller works.
6. If it works, submit a Pull Request to the GitHub repository or send the mapping to me.