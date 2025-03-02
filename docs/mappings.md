# Enhanced Controller Support in RePlay OS

RePlay OS is designed to offer seamless compatibility with a wide range of gamepads and joysticks, thanks to its extensive predefined controller database. This database is built upon the [SDL_GameControllerDB](https://github.com/mdqinc/SDL_GameControllerDB){target=_blank} project, which boasts support for over **700** different controllers and their various revisions, ensuring that most devices work perfectly right out of the box.

## Custom Controller Mapping

If your gamepad or joystick isn't automatically recognized by RePlay OS, or if the default mappings don't align with your preferences, you have the flexibility to create a custom SDL controller mapping. This can be done easily through the `REPLAY OPTIONS > INPUT > CONTROLLER MAPPER` menu.

### Mapping Process

1. **Access the Controller Mapper**: Navigate to `REPLAY OPTIONS > INPUT > CONTROLLER MAPPER` in the RePlay OS menu.
2. **Start Mapping**: Follow the on-screen instructions to map each button and axis on your controller. Each button mapping has a timeout of 5 seconds; if no input is detected within this period, the button will be skipped.
3. **Save Your Mapping**: Once the mapping process is complete, your custom configuration will be saved to the `<unit>/config/input/sdlusermapsdb.txt` file. The location of this file depends on whether you're using an SD card or USB unit.

## Input Layout Design

RePlay OS employs a universal gamepad layout inspired by the XBOX controller but uses positional button labeling to accommodate the diverse physical layouts of various controllers. This approach minimizes conflicts and ensures a consistent user experience across different devices.

### Visual Mapping Guide

For a clearer understanding of the button mapping process, refer to the visual guide below:

![Mapping Guide](img/mapping_guide.png)

This guide will help you visualize the button positions and ensure accurate mapping for your controller.