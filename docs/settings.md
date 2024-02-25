# System Settings

## Arcade (FBNeo)

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Vertical mode | fbneo-vertical-mode | Rotate display for vertical screens |
| Force 60Hz | fbneo-force-60hz | Ignore game's original refresh rate and try to run it at 60hz instead. It will cause incorrect game speed and frame pacing. It will try to use your monitor's correct refresh rate instead of 60hz if this refresh rate is between 59hz and 61hz. |
| Allow patched romsets | fbneo-allow-patched-romsets | Allow romsets from your system/fbneo/patched/ folder to override your romsets, crcs will be ignored but sizes and names must still match, you need to close content for this setting to take effect |
| Analog Speed | fbneo-analog-speed | Mitigate analog controls speed, some games might require low values to be playable |
| Crosshair emulation | fbneo-lightgun-crosshair-emulation | Change emulated crosshair behavior |
| CPU clock | fbneo-cpu-speed-adjust | Change emulated cpu frequency for various systems, by increasing you can fix native slowdowns in some games, by decreasing you can help performance on low-end devices |
| Hiscores | fbneo-hiscores | Enable high scores support, you also need the file hiscore.dat in your system/fbneo/ folder |
| Samplerate | fbneo-samplerate | Configure samplerate, it could impact performances, closing & starting game again is required |
| Sample Interpolation | fbneo-sample-interpolation | Configure sample interpolation, it could impact performances |
| FM Interpolation | fbneo-fm-interpolation | Configure FM interpolation, it could impact performances |
| LowPass Filter | fbneo-lowpass-filter | Enable LowPass Filter |
| Neo-Geo mode | fbneo-neogeo-mode | Load appropriate bios depending on your choice, under the condition such a bios is compatible with the running game |
| Memory card mode | fbneo-memcard-mode | Change the behavior for the memory card |

## Arcade (MAME)

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Thread Mode | mame_thread_mode | n/a |
| Throttle | mame_throttle | n/a |
| Boot to BIOS | mame_boot_to_bios | n/a |
| Boot to OSD | mame_boot_to_osd | n/a |
| Read Configuration | mame_read_config | n/a |
| Write Configuration | mame_write_config | n/a |
| Save State Naming | mame_saves | n/a |
| Auto Save/Load States | mame_auto_save | n/a |
| Softlists | mame_softlists_enable | n/a |
| Softlist Automatic Media Type | mame_softlists_auto_media | n/a |
| Media Type | mame_media_type | n/a |
| Screen Rotation Mode | mame_rotation_mode | n/a |
| Joystick Deadzone | mame_joystick_deadzone | n/a |
| Joystick Saturation | mame_joystick_saturation | n/a |
| Joystick Threshold | mame_joystick_threshold | n/a |
| Joystick 4-way Simulation | mame_mame_4way_enable | n/a |
| Profile Buttons Per Game | mame_buttons_profiles | n/a |
| Mouse | mame_mouse_enable | n/a |
| Lightgun Mode | mame_lightgun_mode | n/a |
| Lightgun Offscreen Position | mame_lightgun_offscreen_mode | n/a |
| CPU Overclock | mame_cpu_overclock | n/a |

## Arcade (MAME 2K3+)

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| CPU Clock Scale | mame2003-plus_cpu_clock_scale | Used to under or over clock the emulated CPU by a specified percentage. |
| Skip Disclaimer | mame2003-plus_skip_disclaimer | Bypasses a copyright warning from being displayed when loading content. |
| Skip Warnings | mame2003-plus_skip_warnings | Bypasses a warning message from being displayed when loading content containing known issues. |
| Display MAME Menu | mame2003-plus_display_setup | Toggles the visibility of the internal MAME menu. |
| Legacy Remapping | mame2003-plus_mame_remapping | Restart core required. Enables MAME menu input remapping. |
| Autosave Hiscore | mame2003-plus_autosave_hiscore | Recommended to use default which will save the hiscore when closing content. Recursively will save repeatedly the entire time during gameplay. Disabled will bypass the use of the hiscore.dat file entirely. |
| Locate System Files Within a Subfolder | mame2003-plus_core_sys_subfolder | n/a |
| Locate Save Files Within a Subfolder | mame2003-plus_core_save_subfolder | n/a |
| X-Y Device | mame2003-plus_xy_device | Selects a specific x-y coordinates input device to read. |
| Input Interface | mame2003-plus_input_interface | Configures which input types are being read. |
| Allow Input Button to Act as a Toggle Switch | mame2003-plus_input_toggle | Disable to use actual hardware such as a fixed position high/low shifter. |
| Center Joystick Axis for Digital Controls | mame2003-plus_digital_joy_centering | Emulates the center position of an analog joystick when using digital controls. Automatically returns the center position when no direction is being applied. |
| Use Samples | mame2003-plus_use_samples | Restart core required. Allow audio sample files to be loaded when provided in the samples directory. |
| Sample Rate | mame2003-plus_sample_rate | Number of audio samples taken per second. Higher rates provide better quality audio. |
| Brightness | mame2003-plus_brightness | Modifies the brightness level being used. |
| Gamma Correction | mame2003-plus_gamma | Modifies the gamma level being used. |
| TATE Mode | mame2003-plus_tate_mode | When enabled, the display will be rotated to the orientation used by actual hardware. |

## Arcade SEGA Naomi/Atomis

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Region | reicast_region | n/a |
| Language | reicast_language | Changes the language used by the BIOS and by any games that contain multiple languages. |
| HLE BIOS (Restart Required) | reicast_hle_bios | Force use of high-level emulation BIOS. |
| Boot to BIOS (Restart Required) | reicast_boot_to_bios | Boot directly into the Dreamcast BIOS menu. |
| Enable DSP | reicast_enable_dsp | Enable emulation of the Dreamcast's audio DSP (digital signal processor). Improves the accuracy of generated sound, but increases performance requirements. |
| Force Windows CE Mode | reicast_force_wince | Enable full MMU (Memory Management Unit) emulation and other settings for Windows CE games. |
| Allow NAOMI Service Buttons | reicast_allow_service_buttons | Enables SERVICE button for NAOMI, to enter cabinet settings. |
| Set NAOMI Games to Free Play | reicast_force_freeplay | Modify to coin settings of the game to free play. |
| Broadband Adapter Emulation | reicast_emulate_bba | Emulate the ethernet broadband adapter instead of the modem. (Restart Required) |
| Enable UPnP | reicast_upnp | Use UPnP to automatically configure your Internet router for online games. |
| Cable Type | reicast_cable_type | The output signal type. 'TV (Composite)' is the most widely supported. |
| Broadcast Standard | reicast_broadcast | n/a |
| Screen Orientation | reicast_screen_rotation | n/a |
| Alpha Sorting | reicast_alpha_sorting | n/a |
| Full framebuffer emulation | reicast_emulate_framebuffer | Enable full framebuffer emulation in VRAM. This is useful for games that directly read or write the framebuffer in VRAM. When enabled, Internal Resolution is forced to 640x480 and performance may be severely impacted. |
| Enable RTT (Render To Texture) Buffer | reicast_enable_rttb | Copy rendered textures back from the GPU to VRAM. This option is normally enabled for games that require it. When enabled, texture rendering upscaling is disabled and performance may be impacted. |
| Mipmapping | reicast_mipmapping | n/a |
| Fog Effects | reicast_fog | n/a |
| Volume Modifier | reicast_volume_modifier_enable | A Dreamcast GPU feature that is typically used by games to draw object shadows. This should normally be enabled - the performance impact is usually minimal to negligible. |
| Anisotropic Filtering | reicast_anisotropic_filtering | Enhance the quality of textures on surfaces that are at oblique viewing angles with respect to the camera. Higher values are more demanding on the GPU. Changes to this setting only apply after restarting. |
| Texture Filtering | reicast_texture_filtering | The texture filtering mode to use. This can be used to force a certain texture filtering mode on all textures to get a crisper (or smoother) appearance than Default. Values other than Default may cause various rendering issues. Changes to this setti |
| Delay Frame Swapping | reicast_delay_frame_swapping | Useful to avoid flashing screens or glitchy videos. Not recommended on slow platforms. |
| Detect Frame Rate Changes | reicast_detect_vsync_swap_interval | Notify frontend when internal frame rate changes (e.g. from 60 fps to 30 fps). Improves frame pacing in games that run at a locked 30 fps or 20 fps, but should be disabled for games with unlocked (unstable) frame rates (e.g. Ecco the Dolphin, Unreal |
| Native Depth Interpolation | reicast_native_depth_interpolation | Helps with texture corruption and depth issues on AMD GPUs. Can also help Intel GPUs in some cases. |
| Threaded Rendering | reicast_threaded_rendering | Runs the GPU and CPU on different threads. Highly recommended. |
| GD-ROM Fast Loading (inaccurate) | reicast_gdrom_fast_loading | Speeds up GD-ROM loading. |
| Dreamcast 32MB RAM Mod | reicast_dc_32mb_mod | Enables 32MB RAM Mod for Dreamcast. May affect compatibility |
| SH4 CPU under/overclock | reicast_sh4clock | Change the SH4 main CPU clock from the default 200 MHz. Underclocking may help slow platforms. Overclocking may increase the frame rate for some games. Use with caution. |
| Analog Stick Deadzone | reicast_analog_stick_deadzone | n/a |
| Trigger Deadzone | reicast_trigger_deadzone | n/a |
| Digital Triggers | reicast_digital_triggers | n/a |
| Purupuru Pack/Vibration Pack | reicast_enable_purupuru | Enables controller force feedback. |
| Broadcast Digital Outputs | reicast_network_output | Broadcast digital outputs and force-feedback state on TCP port 8000. Compatible with the "-output network" MAME option. |
| Show Light Gun Settings | reicast_show_lightgun_settings | Enable configuration of light gun crosshair display options. NOTE: Quick Menu may need to be toggled for this setting to take effect. |
| Gun Crosshair Size Scaling | reicast_lightgun_crosshair_size_scaling | n/a |
| Gun Crosshair 1 Display | reicast_lightgun1_crosshair | n/a |
| Gun Crosshair 2 Display | reicast_lightgun2_crosshair | n/a |
| Gun Crosshair 3 Display | reicast_lightgun3_crosshair | n/a |
| Gun Crosshair 4 Display | reicast_lightgun4_crosshair | n/a |
| Per-Game Visual Memory Units/Systems (VMU) | reicast_per_content_vmus | When disabled, all games share 4 VMU save files (A1, B1, C1, D1) located in RetroArch's system directory. The 'VMU A1' setting creates a unique VMU 'A1' file in RetroArch's save directory for each game that is launched. The 'All VMUs' setting create |
| Visual Memory Units/Systems (VMU) Sounds | reicast_vmu_sound | When enabled, VMU beeps are played. |
| Show Visual Memory Unit/System (VMU) Display Settings | reicast_show_vmu_screen_settings | Enable configuration of emulated VMU LCD screen visibility, size, position and color. NOTE: Quick Menu may need to be toggled for this setting to take effect. |
| VMU Screen 1 Display | reicast_vmu1_screen_display | n/a |
| VMU Screen 1 Position | reicast_vmu1_screen_position | n/a |
| VMU Screen 1 Size | reicast_vmu1_screen_size_mult | n/a |
| VMU Screen 1 Pixel On Color | reicast_vmu1_pixel_on_color | n/a |
| VMU Screen 1 Pixel Off Color | reicast_vmu1_pixel_off_color | n/a |
| VMU Screen 1 Opacity | reicast_vmu1_screen_opacity | n/a |
| VMU Screen 2 Display | reicast_vmu2_screen_display | n/a |
| VMU Screen 2 Position | reicast_vmu2_screen_position | n/a |
| VMU Screen 2 Size | reicast_vmu2_screen_size_mult | n/a |
| VMU Screen 2 Pixel On Color | reicast_vmu2_pixel_on_color | n/a |
| VMU Screen 2 Pixel Off Color | reicast_vmu2_pixel_off_color | n/a |
| VMU Screen 2 Opacity | reicast_vmu2_screen_opacity | n/a |
| VMU Screen 3 Display | reicast_vmu3_screen_display | n/a |
| VMU Screen 3 Position | reicast_vmu3_screen_position | n/a |
| VMU Screen 3 Size | reicast_vmu3_screen_size_mult | n/a |
| VMU Screen 3 Pixel On Color | reicast_vmu3_pixel_on_color | n/a |
| VMU Screen 3 Pixel Off Color | reicast_vmu3_pixel_off_color | n/a |
| VMU Screen 3 Opacity | reicast_vmu3_screen_opacity | n/a |
| VMU Screen 4 Display | reicast_vmu4_screen_display | n/a |
| VMU Screen 4 Position | reicast_vmu4_screen_position | n/a |
| VMU Screen 4 Size | reicast_vmu4_screen_size_mult | n/a |
| VMU Screen 4 Pixel On Color | reicast_vmu4_pixel_on_color | n/a |
| VMU Screen 4 Pixel Off Color | reicast_vmu4_pixel_off_color | n/a |
| VMU Screen 4 Opacity | reicast_vmu4_screen_opacity | n/a |

## Atari 2600/VCS

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Console display | stella_console | n/a |
| Palette colors | stella_palette | n/a |
| TV effects | stella_filter | n/a |
| NTSC aspect % | stella_ntsc_aspect | n/a |
| PAL aspect % | stella_pal_aspect | n/a |
| Stereo sound | stella_stereo | n/a |
| Phosphor mode | stella_phosphor | n/a |
| Phosphor blend % | stella_phosphor_blend | n/a |
| Paddle joypad sensitivity | stella_paddle_joypad_sensitivity | n/a |
| Paddle analog sensitivity | stella_paddle_analog_sensitivity | n/a |

## Atari 5200

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| BIOS (Restart) | a5200_bios | Set BIOS image. 'Official' loads an original console dump provided by the user, named '5200.rom' and placed in the frontend 'System' directory. 'Internal (Altirra OS)' uses an inbuilt open-source alternative with reduced compatibility. The 'Official |
| Hi-Res Artifacting Mode | a5200_artifacting_mode | Set Hi-Res Artifacting mode used.  Typically dependant on the actual emulated system.  Pick the color combination that pleases you.  None disables artifacting.  Good for games like A.E., Backgammon, Miniature Golf and several Atari 800 to Atari 5200 |
| High Fidelity POKEY (Restart) | a5200_enable_new_pokey | Enable High Fidelity Pokey for better quality sound.  Disable for games that use digital sound (Berzerk) |
| Audio Filter | a5200_low_pass_filter | Enable a low pass audio filter to soften the 'harsh' sound produced by the Atari 5200's POKEY chip. |
| Audio Filter Level | a5200_low_pass_range | Specify the cut-off frequency of the low pass audio filter. A higher value increases the perceived 'strength' of the filter, since a wider range of the high frequency spectrum is attenuated. |
| Controller Hacks | a5200_input_hack | Apply gamepad input hacks required for specific games. 'Dual Stick' maps Player 2's joystick to the right analog stick of Player 1's RetroPad, enabling dual stick control in 'Robotron 2084' and 'Space Dungeon'. 'Swap Ports' maps Player 1 to port 2 a |
| Pause acts as Reset | a5200_pause_is_reset | Pressing the button assigned to Pause will send a reset instead.  Some games like Kangaroo and Pole Position need this in order to change game difficulty or number of players. |
| Digital Joystick Sensitivity | a5200_digital_sensitivity | Set the effective range of the emulated analog joystick when using the gamepad's digital D-Pad for movement. Lower values equate to slower speeds. 'Auto' sets value based on cartridge checksum (requires good ROM dumps). |
| Analog Joystick Sensitivity | a5200_analog_sensitivity | Set the effective range of the emulated analog joystick when using the gamepad's left analog stick for movement. Lower values equate to slower speeds. 'Auto' sets value based on cartridge checksum (requires good ROM dumps). |
| Analog Joystick Response | a5200_analog_response | Configure movement speed response when tilting the gamepad's analog stick. 'Linear': Speed is directly proportional to stick displacement. 'Quadratic': Speed increases quadratically with stick displacement, enabling greater precision when making sma |
| Analog Joystick Deadzone | a5200_analog_deadzone | Set the deadzone of the gamepad's analog sticks. May be used to eliminate controller drift. |
| Analog Device | a5200_analog_device | Set the device used for analog input. |

## Atari 7800

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Audio Filter | prosystem_low_pass_filter | Enables a low pass audio filter to soften the 'harsh' sound produced by the Atari 7800's TIA chip. |
| Audio Filter Level | prosystem_low_pass_range | Specifies the cut-off frequency of the low pass audio filter. A higher value increases the perceived 'strength' of the filter, since a wider range of the high frequency spectrum is attenuated. |
| Dual Stick Controller | prosystem_gamepad_dual_stick_hack | Maps Player 2's joystick to the right analog stick of Player 1's RetroPad. Enables dual stick control in supported games (e.g. Robotron: 2084, T:ME Salvo). |

## Atari Jaguar

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Fast Blitter | virtualjaguar_usefastblitter | Use the faster blitter, it is older and less compatible, it will break some games. |
| Doom Resolution Hack | virtualjaguar_doom_res_hack | Hack to fix the halved resolution in Doom. |
| BIOS | virtualjaguar_bios | Use the Jaguar BIOS, required for some games. |
| PAL (Restart) | virtualjaguar_pal | Emulate a PAL Jaguar instead of NTSC. |
| Port 1 > Numpad Buttons to Keyboard Keys | virtualjaguar_p1_numpad_to_kb | Map Jaguar numpad 0-9, * and # to keyboard keys. 'Number Row Keys' will use 1234567890-= keys, 'Keypad Keys' will use 0123456789/* keypad keys. |
| Port 1 > RetroPad Up | virtualjaguar_p1_retropad_up | n/a |
| Port 1 > RetroPad Down | virtualjaguar_p1_retropad_down | n/a |
| Port 1 > RetroPad Left | virtualjaguar_p1_retropad_left | n/a |
| Port 1 > RetroPad Right | virtualjaguar_p1_retropad_right | n/a |
| Port 1 > RetroPad A | virtualjaguar_p1_retropad_a | n/a |
| Port 1 > RetroPad B | virtualjaguar_p1_retropad_b | n/a |
| Port 1 > RetroPad X | virtualjaguar_p1_retropad_x | n/a |
| Port 1 > RetroPad Y | virtualjaguar_p1_retropad_y | n/a |
| Port 1 > RetroPad Select | virtualjaguar_p1_retropad_select | n/a |
| Port 1 > RetroPad Start | virtualjaguar_p1_retropad_start | n/a |
| Port 1 > RetroPad L1 | virtualjaguar_p1_retropad_l1 | n/a |
| Port 1 > RetroPad R1 | virtualjaguar_p1_retropad_r1 | n/a |
| Port 1 > RetroPad L2 | virtualjaguar_p1_retropad_l2 | n/a |
| Port 1 > RetroPad R2 | virtualjaguar_p1_retropad_r2 | n/a |
| Port 1 > RetroPad L3 | virtualjaguar_p1_retropad_l3 | n/a |
| Port 1 > RetroPad R3 | virtualjaguar_p1_retropad_r3 | n/a |
| Port 1 > RetroPad Left Analog Up | virtualjaguar_p1_retropad_analog_lu | n/a |
| Port 1 > RetroPad Left Analog Down | virtualjaguar_p1_retropad_analog_ld | n/a |
| Port 1 > RetroPad Left Analog Left | virtualjaguar_p1_retropad_analog_ll | n/a |
| Port 1 > RetroPad Left Analog Right | virtualjaguar_p1_retropad_analog_lr | n/a |
| Port 1 > RetroPad Right Analog Up | virtualjaguar_p1_retropad_analog_ru | n/a |
| Port 1 > RetroPad Right Analog Down | virtualjaguar_p1_retropad_analog_rd | n/a |
| Port 1 > RetroPad Right Analog Left | virtualjaguar_p1_retropad_analog_rl | n/a |
| Port 1 > RetroPad Right Analog Right | virtualjaguar_p1_retropad_analog_rr | n/a |
| Port 2 > Numpad Buttons to Keyboard Keys | virtualjaguar_p2_numpad_to_kb | Map Jaguar numpad 0-9, * and # to keyboard keys. 'Number Row Keys' will use 1234567890-= keys, 'Keypad Keys' will use 0123456789/* keypad keys. |
| Port 2 > RetroPad Up | virtualjaguar_p2_retropad_up | n/a |
| Port 2 > RetroPad Down | virtualjaguar_p2_retropad_down | n/a |
| Port 2 > RetroPad Left | virtualjaguar_p2_retropad_left | n/a |
| Port 2 > RetroPad Right | virtualjaguar_p2_retropad_right | n/a |
| Port 2 > RetroPad A | virtualjaguar_p2_retropad_a | n/a |
| Port 2 > RetroPad B | virtualjaguar_p2_retropad_b | n/a |
| Port 2 > RetroPad X | virtualjaguar_p2_retropad_x | n/a |
| Port 2 > RetroPad Y | virtualjaguar_p2_retropad_y | n/a |
| Port 2 > RetroPad Select | virtualjaguar_p2_retropad_select | n/a |
| Port 2 > RetroPad Start | virtualjaguar_p2_retropad_start | n/a |
| Port 2 > RetroPad L1 | virtualjaguar_p2_retropad_l1 | n/a |
| Port 2 > RetroPad R1 | virtualjaguar_p2_retropad_r1 | n/a |
| Port 2 > RetroPad L2 | virtualjaguar_p2_retropad_l2 | n/a |
| Port 2 > RetroPad R2 | virtualjaguar_p2_retropad_r2 | n/a |
| Port 2 > RetroPad L3 | virtualjaguar_p2_retropad_l3 | n/a |
| Port 2 > RetroPad R3 | virtualjaguar_p2_retropad_r3 | n/a |
| Port 2 > RetroPad Left Analog Up | virtualjaguar_p2_retropad_analog_lu | n/a |
| Port 2 > RetroPad Left Analog Down | virtualjaguar_p2_retropad_analog_ld | n/a |
| Port 2 > RetroPad Left Analog Left | virtualjaguar_p2_retropad_analog_ll | n/a |
| Port 2 > RetroPad Left Analog Right | virtualjaguar_p2_retropad_analog_lr | n/a |
| Port 2 > RetroPad Right Analog Up | virtualjaguar_p2_retropad_analog_ru | n/a |
| Port 2 > RetroPad Right Analog Down | virtualjaguar_p2_retropad_analog_rd | n/a |
| Port 2 > RetroPad Right Analog Left | virtualjaguar_p2_retropad_analog_rl | n/a |
| Port 2 > RetroPad Right Analog Right | virtualjaguar_p2_retropad_analog_rr | n/a |

## Atari Lynx

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Auto-rotate Screen | lynx_rot_screen | Virtually rotate screen orientation and button mappings automatically for known games. When set to 'Manual', screen rotation is adjusted by pressing the SELECT button, otherwise a fixed rotation can be set to either 0, 90, 180 or 270 degrees counter |
| Force 60Hz | lynx_force_60hz | Force 60Hz instead of original 75Hz refresh rate, for perfectly smooth movement on 60Hz displays |

## NEC TurboGrafx-16/PC Engine

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| **Raspberry Pi 4 and higher** {: colspan=3} |
| Color Palette | pce_palette | Composite tries to recreate the original console output and can show more details in some games. |
| High Resolution Blending Strength | pce_hires_blend | Blend pixels together when in High Resolution mode. Higher values will blur the picture more. |
| PSG Audio Chip (Restart Required) | pce_psgrevision | HuC6280 represents the original PC Engine, HuC6280A the SuperGrafx and CoreGrafx I. |
| Owl Resampler Quality | pce_resamp_quality | Higher values give better signal-to-noise ratio and preservation of higher frequencies but increase the computation cost and may cause higher latency and clipping if the volume is set too high. |
| Mouse Sensitivity | pce_mouse_sensitivity | Higher values will make the mouse cursor move faster. |
| Allow Opposing Directions | pce_up_down_allowed | Enabling this will allow pressing / quickly alternating / holding both left and right (or up and down) directions at the same time. This may cause movement-based glitches. |
| Disable Soft Reset (RUN+SELECT) | pce_disable_softreset | When RUN and SELECT are pressed simultaneously, disable both buttons temporarily instead of resetting. |
| Multitap 5-port Controller | pce_multitap | Enable up to 5-player multitap emulation. Disabling this is only needed in some cases (e.g. Cho Aniki). |
| P1 Default Joypad Type | pce_default_joypad_type_p1 | Choose if port 1 joypad should be 2 or 6 buttons by default. This option is only applied when the core starts, if you want to switch while content is running, use the 'Mode Switch' button. NOTE: 6 buttons joypad can have weird behaviors in non compa |
| P2 Default Joypad Type | pce_default_joypad_type_p2 | Choose if port 2 joypad should be 2 or 6 buttons by default. This option is only applied when the core starts, if you want to switch while content is running, use the 'Mode Switch' button. NOTE: 6 buttons joypad can have weird behaviors in non compa |
| P3 Default Joypad Type | pce_default_joypad_type_p3 | Choose if port 3 joypad should be 2 or 6 buttons by default. This option is only applied when the core starts, if you want to switch while content is running, use the 'Mode Switch' button. NOTE: 6 buttons joypad can have weird behaviors in non compa |
| P4 Default Joypad Type | pce_default_joypad_type_p4 | Choose if port 4 joypad should be 2 or 6 buttons by default. This option is only applied when the core starts, if you want to switch while content is running, use the 'Mode Switch' button. NOTE: 6 buttons joypad can have weird behaviors in non compa |
| P5 Default Joypad Type | pce_default_joypad_type_p5 | Choose if port 5 joypad should be 2 or 6 buttons by default. This option is only applied when the core starts, if you want to switch while content is running, use the 'Mode Switch' button. NOTE: 6 buttons joypad can have weird behaviors in non compa |
| Turbo Hotkey Mode | pce_Turbo_Toggling | Enable turbo buttons. Hotkeys (buttons III and IV) can behave as either toggle switches or dedicated (hold to use) turbo buttons. |
| Alternate Turbo Hotkey | pce_turbo_toggle_hotkey | Assign RetroPad's L3/R3 buttons as turbo hotkeys instead of buttons III and IV. Works only in 'Toggle' mode and only as long as nothing is assigned to the L3/R3 buttons. You can avoid remapping buttons III and IV when switching to 6-button controlle |
| Turbo Speed | pce_Turbo_Delay | Choose how fast button presses are repeated. |
| P1 Turbo I | pce_p0_turbo_I_enable | n/a |
| P1 Turbo II | pce_p0_turbo_II_enable | n/a |
| P2 Turbo I | pce_p1_turbo_I_enable | n/a |
| P2 Turbo II | pce_p1_turbo_II_enable | n/a |
| P3 Turbo I | pce_p2_turbo_I_enable | n/a |
| P3 Turbo II | pce_p2_turbo_II_enable | n/a |
| P4 Turbo I | pce_p3_turbo_I_enable | n/a |
| P4 Turbo II | pce_p3_turbo_II_enable | n/a |
| P5 Turbo I | pce_p4_turbo_I_enable | n/a |
| P5 Turbo II | pce_p4_turbo_II_enable | n/a |
| No Sprite Limit | pce_nospritelimit | Remove 16-sprites-per-scanline hardware limit. WARNING: May cause graphics glitching on some games (such as Bloody Wolf). |
| CPU Overclock Multiplier | pce_ocmultiplier | Higher values can reduce slowdowns in games. WARNING: Can cause glitches and crashes. |
| CD Image Cache (Restart Required) | pce_cdimagecache | Load the complete image into memory at startup. Can potentially decrease loading times at the cost of an increased startup time. |
| CD Bios (Restart Required) | pce_cdbios | Most games can run on 'System Card 3'. 'Games Express' is needed for several unlicensed games. |
| Arcade Card (Restart Required) | pce_arcadecard | Leave this option enabled to allow enhanced modes of ACD-enhanced SCD games. |
| (CD) CD Speed | pce_cdspeed | Higher values enable faster loading times but can cause issues with a couple of games. |
| (CD) ADPCM precision | pce_adpcmextraprec | Full precision of 12-bits for the MSM5205 ADPCM predictor can reduce whining noise during ADPCM playback. |
| (CD) ADPCM Volume % | pce_adpcmvolume | CD game only. Setting this volume control too high may cause sample clipping. |
| (CD) CDDA Volume % | pce_cddavolume | CD game only. Setting this volume control too high may cause sample clipping. |
| (CD) CD PSG Volume % | pce_cdpsgvolume | CD game only. Setting this volume control too high may cause sample clipping. |
| **Raspberry Pi 3 / Zero 2** {: colspan=3} |
| Color Palette | sgx_palette | Composite tries to recreate the original console output and can show more details in some games. |
| Mouse Sensitivity | sgx_mouse_sensitivity | Higher values will make the mouse cursor move faster. |
| Allow Opposing Directions | sgx_up_down_allowed | Enabling this will allow pressing / quickly alternating / holding both left and right (or up and down) directions at the same time. This may cause movement-based glitches. |
| Disable Soft Reset (RUN+SELECT) | sgx_disable_softreset | When RUN and SELECT are pressed simultaneously, disable both buttons temporarily instead of resetting. |
| Multitap 5-port Controller | sgx_multitap | Enable up to 5-player multitap emulation. Disabling this is only needed in some cases (e.g. Cho Aniki). |
| P1 Default Joypad Type | sgx_default_joypad_type_p1 | Choose if port 1 joypad should be 2 or 6 buttons by default. This option is only applied when the core starts, if you want to switch while content is running, use the 'Mode Switch' button. NOTE: 6 buttons joypad can have weird behaviors in non compa |
| P2 Default Joypad Type | sgx_default_joypad_type_p2 | Choose if port 2 joypad should be 2 or 6 buttons by default. This option is only applied when the core starts, if you want to switch while content is running, use the 'Mode Switch' button. NOTE: 6 buttons joypad can have weird behaviors in non compa |
| P3 Default Joypad Type | sgx_default_joypad_type_p3 | Choose if port 3 joypad should be 2 or 6 buttons by default. This option is only applied when the core starts, if you want to switch while content is running, use the 'Mode Switch' button. NOTE: 6 buttons joypad can have weird behaviors in non compa |
| P4 Default Joypad Type | sgx_default_joypad_type_p4 | Choose if port 4 joypad should be 2 or 6 buttons by default. This option is only applied when the core starts, if you want to switch while content is running, use the 'Mode Switch' button. NOTE: 6 buttons joypad can have weird behaviors in non compa |
| P5 Default Joypad Type | sgx_default_joypad_type_p5 | Choose if port 5 joypad should be 2 or 6 buttons by default. This option is only applied when the core starts, if you want to switch while content is running, use the 'Mode Switch' button. NOTE: 6 buttons joypad can have weird behaviors in non compa |
| Turbo Hotkey Mode | sgx_turbo_toggle | Enable turbo buttons. Hotkeys (buttons III and IV) can behave as either toggle switches or dedicated (hold to use) turbo buttons. |
| Alternate Turbo Hotkey | sgx_turbo_toggle_hotkey | Assign RetroPad's L3/R3 buttons as turbo hotkeys instead of buttons III and IV. Works only in 'Toggle' mode and only as long as nothing is assigned to the L3/R3 buttons. You can avoid remapping buttons III and IV when switching to 6-button controlle |
| Turbo Delay | sgx_turbo_delay | Adjust the time between turbo fire (in frames). |
| Input | input | n/a |
| Force SuperGrafx Emulation (Restart Required) | sgx_forcesgx | This is helpful to run homebrew games or to isolate games that will not run in SuperGrafx mode (like Space Harrier). Save states are not compatible with each mode. It's better to leave this option off unless needed. Known SuperGrafx games (like Dai- |
| No Sprite Limit | sgx_nospritelimit | Remove 16-sprites-per-scanline hardware limit. WARNING: May cause graphics glitching on some games. |
| CPU Overclock Multiplier (Restart Required) | sgx_ocmultiplier | Higher values can reduce slowdowns in games. WARNING: Can cause glitches and crashes. |
| CD Image Cache (Restart Required) | sgx_cdimagecache | Load the complete image into memory at startup. Can potentially decrease loading times at the cost of an increased startup time. |
| CD BIOS (Restart Required) | sgx_cdbios | Most games can run on 'System Card 3'. 'Games Express' is needed for several unlicensed games. |
| Detect Games Express CD (Restart Required) | sgx_detect_gexpress | Automatically load the Games Express BIOS regardless of CD BIOS setting when loading Games Express CD games. |
| (CD) CD Speed | sgx_cdspeed | Higher values enable faster loading times but can cause issues with a couple of games. |
| (CD) ADPCM Volume % | sgx_adpcmvolume | CD game only. Setting this volume control too high may cause sample clipping. |
| (CD) CDDA Volume % | sgx_cddavolume | CD game only. Setting this volume control too high may cause sample clipping. |
| (CD) PSG Volume % | sgx_cdpsgvolume | CD game only. Setting this volume control too high may cause sample clipping. |

## NEC TurboGrafx-CD/CD-ROM2 System

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| **Raspberry Pi 4 and higher** {: colspan=3} |
| Color Palette | pce_palette | Composite tries to recreate the original console output and can show more details in some games. |
| High Resolution Blending Strength | pce_hires_blend | Blend pixels together when in High Resolution mode. Higher values will blur the picture more. |
| PSG Audio Chip (Restart Required) | pce_psgrevision | HuC6280 represents the original PC Engine, HuC6280A the SuperGrafx and CoreGrafx I. |
| Owl Resampler Quality | pce_resamp_quality | Higher values give better signal-to-noise ratio and preservation of higher frequencies but increase the computation cost and may cause higher latency and clipping if the volume is set too high. |
| Mouse Sensitivity | pce_mouse_sensitivity | Higher values will make the mouse cursor move faster. |
| Allow Opposing Directions | pce_up_down_allowed | Enabling this will allow pressing / quickly alternating / holding both left and right (or up and down) directions at the same time. This may cause movement-based glitches. |
| Disable Soft Reset (RUN+SELECT) | pce_disable_softreset | When RUN and SELECT are pressed simultaneously, disable both buttons temporarily instead of resetting. |
| Multitap 5-port Controller | pce_multitap | Enable up to 5-player multitap emulation. Disabling this is only needed in some cases (e.g. Cho Aniki). |
| P1 Default Joypad Type | pce_default_joypad_type_p1 | Choose if port 1 joypad should be 2 or 6 buttons by default. This option is only applied when the core starts, if you want to switch while content is running, use the 'Mode Switch' button. NOTE: 6 buttons joypad can have weird behaviors in non compa |
| P2 Default Joypad Type | pce_default_joypad_type_p2 | Choose if port 2 joypad should be 2 or 6 buttons by default. This option is only applied when the core starts, if you want to switch while content is running, use the 'Mode Switch' button. NOTE: 6 buttons joypad can have weird behaviors in non compa |
| P3 Default Joypad Type | pce_default_joypad_type_p3 | Choose if port 3 joypad should be 2 or 6 buttons by default. This option is only applied when the core starts, if you want to switch while content is running, use the 'Mode Switch' button. NOTE: 6 buttons joypad can have weird behaviors in non compa |
| P4 Default Joypad Type | pce_default_joypad_type_p4 | Choose if port 4 joypad should be 2 or 6 buttons by default. This option is only applied when the core starts, if you want to switch while content is running, use the 'Mode Switch' button. NOTE: 6 buttons joypad can have weird behaviors in non compa |
| P5 Default Joypad Type | pce_default_joypad_type_p5 | Choose if port 5 joypad should be 2 or 6 buttons by default. This option is only applied when the core starts, if you want to switch while content is running, use the 'Mode Switch' button. NOTE: 6 buttons joypad can have weird behaviors in non compa |
| Turbo Hotkey Mode | pce_Turbo_Toggling | Enable turbo buttons. Hotkeys (buttons III and IV) can behave as either toggle switches or dedicated (hold to use) turbo buttons. |
| Alternate Turbo Hotkey | pce_turbo_toggle_hotkey | Assign RetroPad's L3/R3 buttons as turbo hotkeys instead of buttons III and IV. Works only in 'Toggle' mode and only as long as nothing is assigned to the L3/R3 buttons. You can avoid remapping buttons III and IV when switching to 6-button controlle |
| Turbo Speed | pce_Turbo_Delay | Choose how fast button presses are repeated. |
| P1 Turbo I | pce_p0_turbo_I_enable | n/a |
| P1 Turbo II | pce_p0_turbo_II_enable | n/a |
| P2 Turbo I | pce_p1_turbo_I_enable | n/a |
| P2 Turbo II | pce_p1_turbo_II_enable | n/a |
| P3 Turbo I | pce_p2_turbo_I_enable | n/a |
| P3 Turbo II | pce_p2_turbo_II_enable | n/a |
| P4 Turbo I | pce_p3_turbo_I_enable | n/a |
| P4 Turbo II | pce_p3_turbo_II_enable | n/a |
| P5 Turbo I | pce_p4_turbo_I_enable | n/a |
| P5 Turbo II | pce_p4_turbo_II_enable | n/a |
| No Sprite Limit | pce_nospritelimit | Remove 16-sprites-per-scanline hardware limit. WARNING: May cause graphics glitching on some games (such as Bloody Wolf). |
| CPU Overclock Multiplier | pce_ocmultiplier | Higher values can reduce slowdowns in games. WARNING: Can cause glitches and crashes. |
| CD Image Cache (Restart Required) | pce_cdimagecache | Load the complete image into memory at startup. Can potentially decrease loading times at the cost of an increased startup time. |
| CD Bios (Restart Required) | pce_cdbios | Most games can run on 'System Card 3'. 'Games Express' is needed for several unlicensed games. |
| Arcade Card (Restart Required) | pce_arcadecard | Leave this option enabled to allow enhanced modes of ACD-enhanced SCD games. |
| (CD) CD Speed | pce_cdspeed | Higher values enable faster loading times but can cause issues with a couple of games. |
| (CD) ADPCM precision | pce_adpcmextraprec | Full precision of 12-bits for the MSM5205 ADPCM predictor can reduce whining noise during ADPCM playback. |
| (CD) ADPCM Volume % | pce_adpcmvolume | CD game only. Setting this volume control too high may cause sample clipping. |
| (CD) CDDA Volume % | pce_cddavolume | CD game only. Setting this volume control too high may cause sample clipping. |
| (CD) CD PSG Volume % | pce_cdpsgvolume | CD game only. Setting this volume control too high may cause sample clipping. |
| **Raspberry Pi 3 / Zero 2** {: colspan=3} |
| Color Palette | sgx_palette | Composite tries to recreate the original console output and can show more details in some games. |
| Mouse Sensitivity | sgx_mouse_sensitivity | Higher values will make the mouse cursor move faster. |
| Allow Opposing Directions | sgx_up_down_allowed | Enabling this will allow pressing / quickly alternating / holding both left and right (or up and down) directions at the same time. This may cause movement-based glitches. |
| Disable Soft Reset (RUN+SELECT) | sgx_disable_softreset | When RUN and SELECT are pressed simultaneously, disable both buttons temporarily instead of resetting. |
| Multitap 5-port Controller | sgx_multitap | Enable up to 5-player multitap emulation. Disabling this is only needed in some cases (e.g. Cho Aniki). |
| P1 Default Joypad Type | sgx_default_joypad_type_p1 | Choose if port 1 joypad should be 2 or 6 buttons by default. This option is only applied when the core starts, if you want to switch while content is running, use the 'Mode Switch' button. NOTE: 6 buttons joypad can have weird behaviors in non compa |
| P2 Default Joypad Type | sgx_default_joypad_type_p2 | Choose if port 2 joypad should be 2 or 6 buttons by default. This option is only applied when the core starts, if you want to switch while content is running, use the 'Mode Switch' button. NOTE: 6 buttons joypad can have weird behaviors in non compa |
| P3 Default Joypad Type | sgx_default_joypad_type_p3 | Choose if port 3 joypad should be 2 or 6 buttons by default. This option is only applied when the core starts, if you want to switch while content is running, use the 'Mode Switch' button. NOTE: 6 buttons joypad can have weird behaviors in non compa |
| P4 Default Joypad Type | sgx_default_joypad_type_p4 | Choose if port 4 joypad should be 2 or 6 buttons by default. This option is only applied when the core starts, if you want to switch while content is running, use the 'Mode Switch' button. NOTE: 6 buttons joypad can have weird behaviors in non compa |
| P5 Default Joypad Type | sgx_default_joypad_type_p5 | Choose if port 5 joypad should be 2 or 6 buttons by default. This option is only applied when the core starts, if you want to switch while content is running, use the 'Mode Switch' button. NOTE: 6 buttons joypad can have weird behaviors in non compa |
| Turbo Hotkey Mode | sgx_turbo_toggle | Enable turbo buttons. Hotkeys (buttons III and IV) can behave as either toggle switches or dedicated (hold to use) turbo buttons. |
| Alternate Turbo Hotkey | sgx_turbo_toggle_hotkey | Assign RetroPad's L3/R3 buttons as turbo hotkeys instead of buttons III and IV. Works only in 'Toggle' mode and only as long as nothing is assigned to the L3/R3 buttons. You can avoid remapping buttons III and IV when switching to 6-button controlle |
| Turbo Delay | sgx_turbo_delay | Adjust the time between turbo fire (in frames). |
| Input | input | n/a |
| Force SuperGrafx Emulation (Restart Required) | sgx_forcesgx | This is helpful to run homebrew games or to isolate games that will not run in SuperGrafx mode (like Space Harrier). Save states are not compatible with each mode. It's better to leave this option off unless needed. Known SuperGrafx games (like Dai- |
| No Sprite Limit | sgx_nospritelimit | Remove 16-sprites-per-scanline hardware limit. WARNING: May cause graphics glitching on some games. |
| CPU Overclock Multiplier (Restart Required) | sgx_ocmultiplier | Higher values can reduce slowdowns in games. WARNING: Can cause glitches and crashes. |
| CD Image Cache (Restart Required) | sgx_cdimagecache | Load the complete image into memory at startup. Can potentially decrease loading times at the cost of an increased startup time. |
| CD BIOS (Restart Required) | sgx_cdbios | Most games can run on 'System Card 3'. 'Games Express' is needed for several unlicensed games. |
| Detect Games Express CD (Restart Required) | sgx_detect_gexpress | Automatically load the Games Express BIOS regardless of CD BIOS setting when loading Games Express CD games. |
| (CD) CD Speed | sgx_cdspeed | Higher values enable faster loading times but can cause issues with a couple of games. |
| (CD) ADPCM Volume % | sgx_adpcmvolume | CD game only. Setting this volume control too high may cause sample clipping. |
| (CD) CDDA Volume % | sgx_cddavolume | CD game only. Setting this volume control too high may cause sample clipping. |
| (CD) PSG Volume % | sgx_cdpsgvolume | CD game only. Setting this volume control too high may cause sample clipping. |

## Nintendo NES/Famicom

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Region | fceumm_region | Force core to use NTSC, PAL or Dendy region timings. |
| Game Genie Add-On (Restart Required) | fceumm_game_genie | Enable emulation of a Game Genie add-on cartridge, allowing cheat codes to be entered when launching games. The Game Genie ROM file 'gamegenie.nes' must be present in the frontend's system directory. Does not apply to FDS or arcade content. |
| Color Palette | fceumm_palette | Choose from pre-generated palettes, a custom 64x3 palette from file or raw format (needs to use a nes-decoder shader). |
| NTSC Filter | fceumm_ntsc_filter | Blargg's NTSC filters are used to replicate RF, Composite, S-Video, and RGB cable signals. |
| Sound Quality | fceumm_sndquality | Enable higher quality sound. Increases performance requirements. |
| Audio RF Filter | fceumm_sndlowpass | Apply a low pass audio filter to simulate the 'muted' sound of the NES when connected to a television via the RF modulator. |
| Stereo Sound Effect | fceumm_sndstereodelay | Enable a fake stereo sound effect by delaying the right audio channel when upmixing the mono signal output from the NES. |
| Swap Audio Duty Cycles | fceumm_swapduty | Simulates the sound from famiclones that have the pulse wave channels duty cycle bits reversed. |
| Master Volume | fceumm_sndvolume | Change master volume level. |
| Audio Channel 1 (Square 1) | fceumm_apu_1 | Enables or disables pulse wave generator audio output 1. |
| Audio Channel 2 (Square 2) | fceumm_apu_2 | Enables or disables pulse wave generator audio output 2. |
| Audio Channel 3 (Triangle) | fceumm_apu_3 | Enables or disables triangle wave generator audio output. |
| Audio Channel 4 (Noise) | fceumm_apu_4 | Enables or disables noise generator audio output. |
| Audio Channel 5 (PCM) | fceumm_apu_5 | Enables or disables delta modulation channel audio output. |
| Turbo Enable | fceumm_turbo_enable | Enables or disables turbo buttons. |
| Turbo Delay (in frames) | fceumm_turbo_delay | Repeat rate of turbo buttons in frames. |
| Zapper Mode | fceumm_zapper_mode | Selects device to use for Zapper games. |
| Show Zapper Crosshair | fceumm_show_crosshair | Shows or hides on-screen crosshairs when using a Zapper. |
| Zapper Tolerance | fceumm_zapper_tolerance | Sets how many pixels from target area is on target. |
| Invert Zapper Trigger Signal | fceumm_zapper_trigger | Inverts trigger logic when using a Zapper. Disabling it resembles original hardware behavior. |
| Invert Zapper Sensor Signal | fceumm_zapper_sensor | Inverts sensor logic when using a Zapper (Sequential Targets Light gun mode only). Disabling it resembles original NES/FC hardware behavior. |
| Arkanoid Mode | fceumm_arkanoid_mode | Selects device to use for Arkanoid games. |
| Mouse Sensitivity | fceumm_mouse_sensitivity | Mouse sensitivity in percent. |
| Allow Opposing Directions | fceumm_up_down_allowed | Allows simultaneous UP+DOWN or LEFT+RIGHT button combinations, which can create different effects in some games. |
| No Sprite Limit | fceumm_nospritelimit | Removes the 8-per-scanline hardware limit. This reduces sprite flickering but can cause some games to glitch since some use this for effects. |
| Overclock | fceumm_overclocking | Enables or disables overclocking, which can reduce slowdowns in some games. Postrender method is more compatible with every game, Vblank is more effective for games like Contra Force. |
| RAM Power-On Fill (Restart Required) | fceumm_ramstate | RAM values on power up. Some games rely on initial RAM values for random number generation as an example. |

## Nintendo Super Nintendo/Super Famicom

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| **Raspberry Pi 4 and higher** {: colspan=3} |
| Console Region (Reload Core) | snes9x_region | Specify which region the system is from. 'PAL' is 50hz, 'NTSC' is 60hz. Games will run faster or slower than normal if the incorrect region is selected. |
| Hi-Res Blending | snes9x_hires_blend | Blend adjacent pixels when game switches to hi-res mode (512x448). Required for certain games that use hi-res mode to produce transparency effects (Kirby's Dream Land, Jurassic Park...). |
| Blargg NTSC Filter | snes9x_blargg | Apply a video filter to mimic various NTSC TV signals. |
| Audio Interpolation | snes9x_audio_interpolation | Apply an audio filter. 'Gaussian' reproduces the bass-heavy sound of the original hardware. 'Cubic' and 'Sinc' are less accurate, and preserve more of the high range. |
| Allow Opposing Directions | snes9x_up_down_allowed | Enabling this will allow pressing / quickly alternating / holding both left and right (or up and down) directions at the same time. This may cause movement-based glitches. |
| Show Light Gun Settings | snes9x_show_lightgun_settings | Enable configuration of Super Scope / Justifier / M.A.C.S. rifle input. NOTE: Quick Menu must be toggled for this setting to take effect. |
| SuperFX Overclocking | snes9x_overclock_superfx | SuperFX coprocessor frequency multiplier. Can improve frame rate or cause timing errors. Values under 100% can improve game performance on slow devices. |
| Reduce Slowdown (Hack, Unsafe) | snes9x_overclock_cycles | Overclock SNES CPU. May cause games to crash! Use 'Light' for shorter loading times, 'Compatible' for most games exhibiting slowdown and 'Max' only if absolutely required (Gradius 3, Super R-type...). |
| Reduce Flickering (Hack, Unsafe) | snes9x_reduce_sprite_flicker | Increases number of sprites that can be drawn simultaneously on screen. |
| Randomize Memory (Unsafe) | snes9x_randomize_memory | Randomizes system RAM upon start-up. Some games such as 'Super Off Road' use system RAM as a random number generator for item placement and AI behavior, to make gameplay more unpredictable. |
| Block Invalid VRAM Access | snes9x_block_invalid_vram_access | Some homebrew/ROM hacks require this option to be disabled for correct operation. |
| Echo Buffer Hack (Unsafe, only enable for old addmusic hacks) | snes9x_echo_buffer_hack | Some homebrew/ROM hacks require this option to be enabled for correct operation. |
| Light Gun Mode | snes9x_lightgun_mode | Use a mouse-controlled 'Light Gun' or 'Touchscreen' input. |
| Super Scope Reverse Trigger Buttons | snes9x_superscope_reverse_buttons | Swap the positions of the Super Scope 'Fire' and 'Cursor' buttons. |
| Super Scope Crosshair | snes9x_superscope_crosshair | Change the crosshair size on screen. |
| Super Scope Color | snes9x_superscope_color | Change the crosshair color on screen. |
| Justifier 1 Crosshair | snes9x_justifier1_crosshair | Change the crosshair size on screen. |
| Justifier 1 Color | snes9x_justifier1_color | Change the crosshair color on screen. |
| Justifier 2 Crosshair | snes9x_justifier2_crosshair | Change the crosshair size on screen. |
| Justifier 2 Color | snes9x_justifier2_color | Change the crosshair color on screen. |
| M.A.C.S. Rifle Crosshair | snes9x_rifle_crosshair | Change the crosshair size on screen. |
| M.A.C.S. Rifle Color | snes9x_rifle_color | Change the crosshair color on screen. |
| Show Layer 1 | snes9x_layer_1 | n/a |
| Show Layer 2 | snes9x_layer_2 | n/a |
| Show Layer 3 | snes9x_layer_3 | n/a |
| Show Layer 4 | snes9x_layer_4 | n/a |
| Show Sprite Layer | snes9x_layer_5 | n/a |
| Enable Graphic Clip Windows | snes9x_gfx_clip | n/a |
| Enable Transparency Effects | snes9x_gfx_transp | n/a |
| Enable Sound Channel 1 | snes9x_sndchan_1 | n/a |
| Enable Sound Channel 2 | snes9x_sndchan_2 | n/a |
| Enable Sound Channel 3 | snes9x_sndchan_3 | n/a |
| Enable Sound Channel 4 | snes9x_sndchan_4 | n/a |
| Enable Sound Channel 5 | snes9x_sndchan_5 | n/a |
| Enable Sound Channel 6 | snes9x_sndchan_6 | n/a |
| Enable Sound Channel 7 | snes9x_sndchan_7 | n/a |
| Enable Sound Channel 8 | snes9x_sndchan_8 | n/a |
| **Raspberry Pi 3 / Zero 2** {: colspan=3} |
| Console Region (Restart) | snes9x_2010_region | Specify which region the system is from. 'PAL' is 50hz, 'NTSC' is 60hz. Games will run faster or slower than normal if the incorrect region is selected. |
| Set Autofire Pulse | snes9x_2010_turbodelay | Fire interval: medium - 6 frames, fast - 4 frames, slow - 8 frames. |
| Blargg NTSC Filter | snes9x_2010_blargg | Apply a video filter to mimic various NTSC TV signals. |
| SuperFX Overclock | snes9x_2010_overclock | Overclock or underclock the SuperFX chip. This may improve the framerate and playability of games that use SuperFX. |
| Reduce Slowdown (Hack, Unsafe) | snes9x_2010_overclock_cycles | Overclock SNES CPU. May cause games to crash! Use 'Light' for shorter loading times, 'Compatible' for most games exhibiting slowdown and 'Max' only if absolutely required (Gradius 3, Super R-type...). |
| Reduce Flickering (Hack, Unsafe) | snes9x_2010_reduce_sprite_flicker | Increases number of sprites that can be drawn simultaneously on screen. |
| Block Invalid VRAM Access (Restart) | snes9x_2010_block_invalid_vram_access | Some homebrew/ROM hacks require this option to be disabled for correct operation. |

## Nintendo 64

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Frame Duplication | mupen64plus-FrameDuping | Enable Frame duplication to improve smoothing on low-end. Different from frameskip. |
| Framerate | mupen64plus-Framerate | Fullspeed will enforce Count per Op 1 and FBEmu settings, this will break some games! |
| VI Refresh (Overclock) | mupen64plus-virefresh | Select a VI Refresh clock, Auto does not impact behaviour, other values override CountPerScanline. |
| Disable Expansion Pak | mupen64plus-ForceDisableExtraMem | Force disable Expansion Pak (might improve performance for some games while reducing emulation accuracy, will break games that require it). |
| Ignore emulated TLB Exceptions | mupen64plus-IgnoreTLBExceptions | (HACK) Ignore emulated TLB Exceptions, this might fix some broken romhacks. This option might be removed in the future. |
| Analog Deadzone (percent) | mupen64plus-astick-deadzone | Size of the non responsive area around an analog stick. |
| Analog Sensitivity (percent) | mupen64plus-astick-sensitivity | Adjust how far the stick needs to be moved to reach its max value. |
| Right C Button | mupen64plus-r-cbutton | Select Right C Button mapping. |
| Left C Button | mupen64plus-l-cbutton | Select Left C Button mapping. |
| Down C Button | mupen64plus-d-cbutton | Select Down C Button mapping. |
| Up C Button | mupen64plus-u-cbutton | Select Up C Button mapping. |
| Independent C-button Controls | mupen64plus-alt-map | Use an alternate control scheme, useful for some 3rdparty controllers. |
| Player 1 Pak | mupen64plus-pak1 | Select Player 1 Controller Pak. |
| Player 2 Pak | mupen64plus-pak2 | Select Player 2 Controller Pak. |
| Player 3 Pak | mupen64plus-pak3 | Select Player 3 Controller Pak. |
| Player 4 Pak | mupen64plus-pak4 | Select Player 4 Controller Pak. |
| Threaded Renderer | mupen64plus-ThreadedRenderer | (GLN64) Use the Threaded Renderer, improves performance but increases input lag. |
| Bilinear filtering mode | mupen64plus-BilinearMode | (GLN64) Select a Bilinear filtering method, 3point is the original system specific way. |
| Hybrid Filter | mupen64plus-HybridFilter | (GLN64) Hybrid integer scaling filter, this can be slow with low-end GPUs. |
| Dithering | mupen64plus-DitheringPattern | (GLN64) Applies dithering pattern to output image. |
| Dithering Quantization | mupen64plus-DitheringQuantization | (GLN64) Dither with color quantization. |
| Image Dithering Mode | mupen64plus-RDRAMImageDitheringMode | (GLN64) Dithering mode for image in RDRAM. |
| MSAA level | mupen64plus-MultiSampling | (GLN64) Anti-Aliasing level (0 = disabled). |
| FXAA | mupen64plus-FXAA | (GLN64) Fast Approximate Anti-Aliasing shader, moderately blur textures (0 = disabled). |
| LOD Emulation | mupen64plus-EnableLODEmulation | (GLN64) Calculate per-pixel Level Of Details to select texture mip levels and blend them with each other using LOD fraction. |
| Framebuffer Emulation | mupen64plus-EnableFBEmulation | (GLN64) Frame/depth buffer emulation. Disabling it can shorten input lag for particular games, but also break some special effects. |
| Copy auxiliary buffers to RDRAM | mupen64plus-EnableCopyAuxToRDRAM | (GLN64) Copy auxiliary buffers to RDRAM (fixes some Game artifacts like Paper Mario Intro). |
| Color buffer to RDRAM | mupen64plus-EnableCopyColorToRDRAM | (GLN64) Color buffer copy to RDRAM (Off will trade compatibility for Performance). |
| Depth buffer to RDRAM | mupen64plus-EnableCopyDepthToRDRAM | (GLN64) Depth buffer copy to RDRAM (Off will trade compatibility for Performance). |
| Background Mode | mupen64plus-BackgroundMode | (GLN64) Render backgrounds mode (HLE only). One piece (fast), Stripped (precise). |
| Hardware per-pixel lighting | mupen64plus-EnableHWLighting | (GLN64) Standard per-vertex lighting when disabled. Slightly different rendering. |
| Continuous texrect coords | mupen64plus-CorrectTexrectCoords | (GLN64) Make texrect coordinates continuous to avoid black lines between them. |
| Enable inaccurate texture coordinates | mupen64plus-EnableInaccurateTextureCoordinates | (GLN64) Enables inaccurate texture coordinate calculations. This can improve performance and texture pack compatibity at the cost of accuracy. |
| Enable native-res boundaries for texture coordinates | mupen64plus-EnableTexCoordBounds | (GLN64) Bound texture rectangle texture coordinates to the values they take in native resolutions. It prevents garbage due to fetching out of texture bounds, but can result in hard edges. |
| Native res. 2D texrects | mupen64plus-EnableNativeResTexrects | (GLN64) Render 2D texrects in native resolution to fix misalignment between parts of 2D image (example: Mario Kart driver selection portraits). |
| Less accurate blending mode | mupen64plus-EnableLegacyBlending | (GLN64) Do not use shaders to emulate N64 blending modes. Works faster on slow GPU. Can cause glitches. |
| GPU shader depth write | mupen64plus-EnableFragmentDepthWrite | (GLN64) Enable writing of fragment depth. Some mobile GPUs do not support it, thus it's optional. Leave enabled. |
| Cache Textures | mupen64plus-EnableTextureCache | (GLN64) Save texture cache to hard disk. |
| Max High-Res VRAM Limit | mupen64plus-MaxHiResTxVramLimit | (GLN64) Limit High-Res textures size in VRAM (in MB, 0 = no limit). |
| Max texture cache size | mupen64plus-MaxTxCacheSize | (GLN64) Set Max texture cache size (in elements). Reduce it if you experience black textures leading to a crash. |
| Texture filter | mupen64plus-txFilterMode | (GLN64) Select Texture Filtering mode. |
| Texture Enhancement | mupen64plus-txEnhancementMode | (GLN64) Various Texture Filters ('As-Is' will just cache). |
| Don't filter background textures | mupen64plus-txFilterIgnoreBG | (GLN64) Ignore filtering for Background Textures. |
| INI Behaviour | mupen64plus-GLideN64IniBehaviour | (GLN64) Specifies INI Settings behaviour. This should really only contain essential options. Changing this can and will break ROM's, if the correct options aren't set manually. Some options may only be set via INI (fbInfoDisabled). |

### Dithering Advanced Info

RDRAM image dithering and shader dithering are mostly independent of each other.
Native res + shader dithering provides authentic look, and no post processing is required.

* DitheringPattern: shader dithering is per-polygon and controlled by game.
* RDRAMImageDitheringMode: RDRAM image dithering is post-processing, dithering method controlled by user or hardcoded.
The only case when shader dithering overrides RDRAM image dithering is "native res + shader dithering are both enabled".
* DitheringQuantization: quantization converts RGB to RGB555 and 8Bit alpha to 5Bit alpha if dithering is used. So in theory it should look worse, because you loose precision. On the other hand it looks right, because real hardware is doing the same thing.

Based on the above info, the most authentic look is:

* DitheringPattern = "True"
* DitheringQuantization = "True"
* RDRAMImageDitheringMode = "False"

**Please do note that the above configurations will impact the system performance**

## Nintendo Game Boy

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Game Boy Model (Restart) | mgba_gb_model | Runs loaded content with a specific Game Boy model. 'Autodetect' will select the most appropriate model for the current game. |
| Use BIOS File if Found (Restart) | mgba_use_bios | Use official BIOS/bootloader for emulated hardware, if present in RetroArch's system directory. |
| Skip BIOS Intro (Restart) | mgba_skip_bios | When using an official BIOS/bootloader, skip the start-up logo animation. This setting is ignored when 'Use BIOS File if Found' is disabled. |
| Default Game Boy Palette | mgba_gb_colors | Selects which palette is used for Game Boy games that are not Game Boy Color or Super Game Boy compatible, or if the model is forced to Game Boy. |
| Hardware Preset Game Boy Palettes (Restart) | mgba_gb_colors_preset | Use the palettes for Game Boy games that have presets on the Game Boy Color or Super Game Boy. |
| Use Super Game Boy Borders (Restart) | mgba_sgb_borders | Display Super Game Boy borders when running Super Game Boy enhanced games. |
| Color Correction | mgba_color_correction | Adjusts output colors to match the display of real GBA/GBC hardware. |
| Interframe Blending | mgba_interframe_blending | Simulates LCD ghosting effects. 'Simple' performs a 50:50 mix of the current and previous frames. 'Smart' attempts to detect screen flickering, and only performs a 50:50 mix on affected pixels. 'LCD Ghosting' mimics natural LCD response times by com |
| Audio Filter | mgba_audio_low_pass_filter | Enables a low pass audio filter to reduce the 'harshness' of generated audio. |
| Audio Filter Level | mgba_audio_low_pass_range | Specifies the cut-off frequency of the low pass audio filter. A higher value increases the perceived 'strength' of the filter, since a wider range of the high frequency spectrum is attenuated. |
| Allow Opposing Directional Input | mgba_allow_opposing_directions | Enabling this will allow pressing / quickly alternating / holding both left and right (or up and down) directions at the same time. This may cause movement-based glitches. |
| Solar Sensor Level | mgba_solar_sensor_level | Sets ambient sunlight intensity. Can be used by games that included a solar sensor in their cartridges, e.g: the Boktai series. |
| Game Boy Player Rumble (Restart) | mgba_force_gbp | Enabling this will allow compatible games with the Game Boy Player boot logo to make the controller rumble. Due to how Nintendo decided this feature should work, it may cause glitches such as flickering or lag in some of these games. |
| Idle Loop Removal | mgba_idle_optimization | Reduce system load by optimizing so-called 'idle-loops' - sections in the code where nothing happens, but the CPU runs at full speed (like a car revving in neutral). Improves performance, and should be enabled on low-end hardware. |

## Nintendo Game Boy Advance

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Game Boy Model (Restart) | mgba_gb_model | Runs loaded content with a specific Game Boy model. 'Autodetect' will select the most appropriate model for the current game. |
| Use BIOS File if Found (Restart) | mgba_use_bios | Use official BIOS/bootloader for emulated hardware, if present in RetroArch's system directory. |
| Skip BIOS Intro (Restart) | mgba_skip_bios | When using an official BIOS/bootloader, skip the start-up logo animation. This setting is ignored when 'Use BIOS File if Found' is disabled. |
| Default Game Boy Palette | mgba_gb_colors | Selects which palette is used for Game Boy games that are not Game Boy Color or Super Game Boy compatible, or if the model is forced to Game Boy. |
| Hardware Preset Game Boy Palettes (Restart) | mgba_gb_colors_preset | Use the palettes for Game Boy games that have presets on the Game Boy Color or Super Game Boy. |
| Use Super Game Boy Borders (Restart) | mgba_sgb_borders | Display Super Game Boy borders when running Super Game Boy enhanced games. |
| Color Correction | mgba_color_correction | Adjusts output colors to match the display of real GBA/GBC hardware. |
| Interframe Blending | mgba_interframe_blending | Simulates LCD ghosting effects. 'Simple' performs a 50:50 mix of the current and previous frames. 'Smart' attempts to detect screen flickering, and only performs a 50:50 mix on affected pixels. 'LCD Ghosting' mimics natural LCD response times by com |
| Audio Filter | mgba_audio_low_pass_filter | Enables a low pass audio filter to reduce the 'harshness' of generated audio. |
| Audio Filter Level | mgba_audio_low_pass_range | Specifies the cut-off frequency of the low pass audio filter. A higher value increases the perceived 'strength' of the filter, since a wider range of the high frequency spectrum is attenuated. |
| Allow Opposing Directional Input | mgba_allow_opposing_directions | Enabling this will allow pressing / quickly alternating / holding both left and right (or up and down) directions at the same time. This may cause movement-based glitches. |
| Solar Sensor Level | mgba_solar_sensor_level | Sets ambient sunlight intensity. Can be used by games that included a solar sensor in their cartridges, e.g: the Boktai series. |
| Game Boy Player Rumble (Restart) | mgba_force_gbp | Enabling this will allow compatible games with the Game Boy Player boot logo to make the controller rumble. Due to how Nintendo decided this feature should work, it may cause glitches such as flickering or lag in some of these games. |
| Idle Loop Removal | mgba_idle_optimization | Reduce system load by optimizing so-called 'idle-loops' - sections in the code where nothing happens, but the CPU runs at full speed (like a car revving in neutral). Improves performance, and should be enabled on low-end hardware. |

## Nintendo DS
| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Console Mode | melonds_console_mode | n/a |
| Boot Game Directly | melonds_boot_directly | Choose if the core should boot the game directly or if it should boot to the DS menu instead (BIOS and firmware files required). |
| Use Firmware Settings | melonds_use_fw_settings | Use language and username from the DS firmware. When disabled or if firmware file was not found, the username will be provided by the Libretro frontend, if it's empty it will default to 'melonDS'. |
| Language | melonds_language | Selected language will be used if 'Use Firmware Settings' is disabled or if firmware file was not found. |
| Randomize MAC Address | melonds_randomize_mac_address | n/a |
| Enable DSi SD Card | melonds_dsi_sdcard | n/a |
| Threaded Software Renderer | melonds_threaded_renderer | n/a |
| Microphone Input | melonds_mic_input | Choose the type of noise that will be used as microphone input. |
| Audio Bitrate | melonds_audio_bitrate | n/a |
| Audio Interpolation | melonds_audio_interpolation | n/a |
| Touch Mode | melonds_touch_mode | Choose mode for interactions with the touch screen. |
| Swap Screen Mode | melonds_swapscreen_mode | Choose if the 'Swap screens' button should work on press or on hold. |
| Screen Layout | melonds_screen_layout | Choose how many screens should be displayed and how they should be displayed. |
| Screen Gap | melonds_screen_gap | Choose how large the gap between the 2 screens should be. |
| Hybrid Small Screen Mode | melonds_hybrid_small_screen | Choose the position of the small screen when using a 'hybrid' mode, or if it should show both screens. |

## SEGA SG-1000

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| System | system | n/a |
| .. | .. | n/a |
| System Hardware | genesis_plus_gx_system_hw | Runs loaded content with a specific emulated console. 'Auto' will select the most appropriate system for the current game. |
| System Region | genesis_plus_gx_region_detect | Specify which region the system is from. For consoles other than the Game Gear, 'PAL' is 50 Hz, while 'NTSC' is 60 Hz. Games may run faster or slower than normal if the incorrect region is selected. |
| System Boot ROM | genesis_plus_gx_bios | Use official BIOS/bootloader for emulated hardware, if present in RetroArch's system directory. Displays console-specific start-up sequence/animation, then runs loaded content. |
| CD System BRAM (Requires Restart) | genesis_plus_gx_system_bram | When running Sega CD/Mega-CD content, specifies whether to share a single save file between all games from a specific region (Per-BIOS) or to create a separate save file for each game (Per-Game). Note that the Sega CD/Mega-CD has limited internal st |
| CD Backup Cart BRAM (Requires Restart) | genesis_plus_gx_cart_bram | When running Sega CD/Mega-CD content, specifies whether to share a single backup ram cart for all games (Per-Cart) or to create a separate backup ram cart for each game (Per-Game). |
| CD Backup Cart BRAM Size (Requires Restart) | genesis_plus_gx_cart_size | Sets the backup ram cart size when running Sega CD/Mega-CD content. Useful when setting the backup ram cart to Per-Game to avoid multiple larger cart sizes. |
| CD add-on (MD mode) (Requires Restart) | genesis_plus_gx_add_on | Specify which add-on to use for CD audio playback with supported Mega Drive/Genesis games. |
| Cartridge Lock-On | genesis_plus_gx_lock_on | Lock-On Technology is a Mega Drive/Genesis feature that allowed an older game to connect to the pass-through port of a special cartridge for extended or altered gameplay. This option specifies which type of special 'lock-on' cartridge to emulate. A  |
| Game Gear Extended Screen | genesis_plus_gx_gg_extra | Forces Game Gear titles to run in SMS mode, with an increased resolution of 256x192. May show additional content, but typically displays a border of corrupt/unwanted image data. |
| Blargg NTSC Filter | genesis_plus_gx_blargg_ntsc_filter | Apply a video filter to mimic various NTSC TV signals. |
| LCD Ghosting Filter | genesis_plus_gx_lcd_filter | Apply an image 'ghosting' filter to mimic the display characteristics of the Game Gear and Genesis Nomad LCD panels. |
| Interlaced Mode 2 Output | genesis_plus_gx_render | Interlaced Mode 2 allows the Mega Drive/Genesis to output a double height (high resolution) 320x448 image by drawing alternate scan lines each frame (this is used by Sonic the Hedgehog 2 and Combat Cars multiplayer modes). 'Double Field' mimics orig |
| Master System FM (YM2413) | genesis_plus_gx_ym2413 | Enable emulation of the FM Sound Unit used by certain Sega Mark III/Master System games for enhanced audio output. |
| Master System FM (YM2413) Core | genesis_plus_gx_ym2413_core | Select method used to emulate the FM Sound Unit of the Sega Mark III/Master System. 'MAME' option is fast, and runs full speed on most systems. 'Nuked' option is cycle accurate, very high quality, and has substantial CPU requirements. |
| Mega Drive/Genesis FM | genesis_plus_gx_ym2612 | Select method used to emulate the FM synthesizer (main sound generator) of the Mega Drive/Genesis. 'MAME' options are fast, and run full speed on most systems. 'Nuked' options are cycle accurate, very high quality, and have substantial CPU requireme |
| Sound Output | genesis_plus_gx_sound_output | Select stereo or mono sound playback. |
| Audio Filter | genesis_plus_gx_audio_filter | Enable a low pass audio filter to better simulate the characteristic sound of a Model 1 Mega Drive/Genesis. |
| Low-Pass Filter % | genesis_plus_gx_lowpass_range | Specify the cut-off frequency of the audio low pass filter. A higher value increases the perceived 'strength' of the filter, since a wider range of the high frequency spectrum is attenuated. |
| PSG Preamp Level | genesis_plus_gx_psg_preamp | Set the audio preamplifier level of the emulated SN76496 4-channel Programmable Sound Generator found in the SG-1000, Sega Mark III, Master System, Game Gear and Mega Drive/Genesis. |
| FM Preamp Level | genesis_plus_gx_fm_preamp | Set the audio preamplifier level of the emulated Mega Drive/Genesis FM sound synthesizer or Sega Mark III/Master System FM Sound Unit. |
| CD-DA Volume | genesis_plus_gx_cdda_volume | Adjust the mixing volume of the emulated CD audio playback output. |
| PCM Volume | genesis_plus_gx_pcm_volume | Adjust the mixing volume of the emulated Sega CD/Mega-CD RF5C164 PCM sound generator output. |
| EQ Low | genesis_plus_gx_audio_eq_low | Adjust the low range band of the internal audio equalizer. |
| EQ Mid | genesis_plus_gx_audio_eq_mid | Adjust the middle range band of the internal audio equalizer. |
| EQ High | genesis_plus_gx_audio_eq_high | Adjust the high range band of the internal audio equalizer. |
| Light Gun Input | genesis_plus_gx_gun_input | Use a mouse-controlled 'Light Gun' or 'Touchscreen' input. |
| Show Light Gun Crosshair | genesis_plus_gx_gun_cursor | Display light gun crosshairs when using the MD Menacer, MD Justifiers and MS Light Phaser input device types. |
| Invert Mouse Y-Axis | genesis_plus_gx_invert_mouse | Inverts the Y-axis of the MD Mouse input device type. |
| Remove Per-Line Sprite Limit | genesis_plus_gx_no_sprite_limit | Removes the original sprite-per-scanline hardware limit. This reduces flickering but can cause visual glitches, as some games exploit the hardware limit to generate special effects. |
| Enhanced per-tile vertical scroll | genesis_plus_gx_enhanced_vscroll | Allows each individual cell to be scrolled vertically, instead of 16px 2-cell, by averaging out with the vscroll value of the neighbouring cell. This hack only applies to few games that use 2-cell vertical scroll mode. |
| Enhanced per-tile vertical scroll limit | genesis_plus_gx_enhanced_vscroll_limit | Only when Enhanced per-tile vertical scroll is enabled. Adjusts the limit of the vertical scroll enhancement. When the vscroll difference between neighbouring tiles is bigger than this limit, the enhancement is disabled. |
| CPU Speed | genesis_plus_gx_overclock | Overclock the emulated CPU. Can reduce slowdown, but may cause glitches. |
| System Lock-Ups | genesis_plus_gx_force_dtack | Emulate system lock-ups that occur on real hardware when performing illegal address access. This should only be disabled when playing certain demos and homebrew that rely on illegal behavior for correct operation. |
| 68K Address Error | genesis_plus_gx_addr_error | The Mega Drive/Genesis main CPU (Motorola 68000) generates an Address Error exception (crash) when attempting to perform unaligned memory access. Enabling this will simulate this behavior. It should only be disabled when playing ROM hacks, since the |
| CD access time | genesis_plus_gx_cd_latency | Simulate original CD hardware latency when initiating a read or seeking to a specific location on loaded disc. This is required by a few CD games that crash if CD data is available too soon and also fixes CD audio desync issues in some games. Disabl |
| PSG Tone Channel 0 Volume % | genesis_plus_gx_psg_channel_0_volume | Reduce the volume of the PSG Tone Channel 0. |
| PSG Tone Channel 1 Volume % | genesis_plus_gx_psg_channel_1_volume | Reduce the volume of the PSG Tone Channel 1. |
| PSG Tone Channel 2 Volume % | genesis_plus_gx_psg_channel_2_volume | Reduce the volume of the PSG Tone Channel 2. |
| PSG Noise Channel 3 Volume % | genesis_plus_gx_psg_channel_3_volume | Reduce the volume of the PSG Noise Channel 3. |
| Mega Drive/Genesis FM Channel 0 Volume % | genesis_plus_gx_md_channel_0_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 0. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 1 Volume % | genesis_plus_gx_md_channel_1_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 1. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 2 Volume % | genesis_plus_gx_md_channel_2_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 2. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 3 Volume % | genesis_plus_gx_md_channel_3_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 3. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 4 Volume % | genesis_plus_gx_md_channel_4_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 4. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 5 Volume % | genesis_plus_gx_md_channel_5_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 5. Only works with MAME FM emulators. |
| Master System FM (YM2413) Channel 0 Volume % | genesis_plus_gx_sms_fm_channel_0_volume | Reduce the volume of the Master System FM Channel 0. |
| Master System FM (YM2413) Channel 1 Volume % | genesis_plus_gx_sms_fm_channel_1_volume | Reduce the volume of the Master System FM Channel 1. |
| Master System FM (YM2413) Channel 2 Volume % | genesis_plus_gx_sms_fm_channel_2_volume | Reduce the volume of the Master System FM Channel 2. |
| Master System FM (YM2413) Channel 3 Volume % | genesis_plus_gx_sms_fm_channel_3_volume | Reduce the volume of the Master System FM Channel 3. |
| Master System FM (YM2413) Channel 4 Volume % | genesis_plus_gx_sms_fm_channel_4_volume | Reduce the volume of the Master System FM Channel 4. |
| Master System FM (YM2413) Channel 5 Volume % | genesis_plus_gx_sms_fm_channel_5_volume | Reduce the volume of the Master System FM Channel 5. |
| Master System FM (YM2413) Channel 6 Volume % | genesis_plus_gx_sms_fm_channel_6_volume | Reduce the volume of the Master System FM Channel 6. |
| Master System FM (YM2413) Channel 7 Volume % | genesis_plus_gx_sms_fm_channel_7_volume | Reduce the volume of the Master System FM Channel 7. |
| Master System FM (YM2413) Channel 8 Volume % | genesis_plus_gx_sms_fm_channel_8_volume | Reduce the volume of the Master System FM Channel 8. |

## SEGA Game Gear

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| System | system | n/a |
| .. | .. | n/a |
| System Hardware | genesis_plus_gx_system_hw | Runs loaded content with a specific emulated console. 'Auto' will select the most appropriate system for the current game. |
| System Region | genesis_plus_gx_region_detect | Specify which region the system is from. For consoles other than the Game Gear, 'PAL' is 50 Hz, while 'NTSC' is 60 Hz. Games may run faster or slower than normal if the incorrect region is selected. |
| System Boot ROM | genesis_plus_gx_bios | Use official BIOS/bootloader for emulated hardware, if present in RetroArch's system directory. Displays console-specific start-up sequence/animation, then runs loaded content. |
| CD System BRAM (Requires Restart) | genesis_plus_gx_system_bram | When running Sega CD/Mega-CD content, specifies whether to share a single save file between all games from a specific region (Per-BIOS) or to create a separate save file for each game (Per-Game). Note that the Sega CD/Mega-CD has limited internal st |
| CD Backup Cart BRAM (Requires Restart) | genesis_plus_gx_cart_bram | When running Sega CD/Mega-CD content, specifies whether to share a single backup ram cart for all games (Per-Cart) or to create a separate backup ram cart for each game (Per-Game). |
| CD Backup Cart BRAM Size (Requires Restart) | genesis_plus_gx_cart_size | Sets the backup ram cart size when running Sega CD/Mega-CD content. Useful when setting the backup ram cart to Per-Game to avoid multiple larger cart sizes. |
| CD add-on (MD mode) (Requires Restart) | genesis_plus_gx_add_on | Specify which add-on to use for CD audio playback with supported Mega Drive/Genesis games. |
| Cartridge Lock-On | genesis_plus_gx_lock_on | Lock-On Technology is a Mega Drive/Genesis feature that allowed an older game to connect to the pass-through port of a special cartridge for extended or altered gameplay. This option specifies which type of special 'lock-on' cartridge to emulate. A  |
| Game Gear Extended Screen | genesis_plus_gx_gg_extra | Forces Game Gear titles to run in SMS mode, with an increased resolution of 256x192. May show additional content, but typically displays a border of corrupt/unwanted image data. |
| Blargg NTSC Filter | genesis_plus_gx_blargg_ntsc_filter | Apply a video filter to mimic various NTSC TV signals. |
| LCD Ghosting Filter | genesis_plus_gx_lcd_filter | Apply an image 'ghosting' filter to mimic the display characteristics of the Game Gear and Genesis Nomad LCD panels. |
| Interlaced Mode 2 Output | genesis_plus_gx_render | Interlaced Mode 2 allows the Mega Drive/Genesis to output a double height (high resolution) 320x448 image by drawing alternate scan lines each frame (this is used by Sonic the Hedgehog 2 and Combat Cars multiplayer modes). 'Double Field' mimics orig |
| Master System FM (YM2413) | genesis_plus_gx_ym2413 | Enable emulation of the FM Sound Unit used by certain Sega Mark III/Master System games for enhanced audio output. |
| Master System FM (YM2413) Core | genesis_plus_gx_ym2413_core | Select method used to emulate the FM Sound Unit of the Sega Mark III/Master System. 'MAME' option is fast, and runs full speed on most systems. 'Nuked' option is cycle accurate, very high quality, and has substantial CPU requirements. |
| Mega Drive/Genesis FM | genesis_plus_gx_ym2612 | Select method used to emulate the FM synthesizer (main sound generator) of the Mega Drive/Genesis. 'MAME' options are fast, and run full speed on most systems. 'Nuked' options are cycle accurate, very high quality, and have substantial CPU requireme |
| Sound Output | genesis_plus_gx_sound_output | Select stereo or mono sound playback. |
| Audio Filter | genesis_plus_gx_audio_filter | Enable a low pass audio filter to better simulate the characteristic sound of a Model 1 Mega Drive/Genesis. |
| Low-Pass Filter % | genesis_plus_gx_lowpass_range | Specify the cut-off frequency of the audio low pass filter. A higher value increases the perceived 'strength' of the filter, since a wider range of the high frequency spectrum is attenuated. |
| PSG Preamp Level | genesis_plus_gx_psg_preamp | Set the audio preamplifier level of the emulated SN76496 4-channel Programmable Sound Generator found in the SG-1000, Sega Mark III, Master System, Game Gear and Mega Drive/Genesis. |
| FM Preamp Level | genesis_plus_gx_fm_preamp | Set the audio preamplifier level of the emulated Mega Drive/Genesis FM sound synthesizer or Sega Mark III/Master System FM Sound Unit. |
| CD-DA Volume | genesis_plus_gx_cdda_volume | Adjust the mixing volume of the emulated CD audio playback output. |
| PCM Volume | genesis_plus_gx_pcm_volume | Adjust the mixing volume of the emulated Sega CD/Mega-CD RF5C164 PCM sound generator output. |
| EQ Low | genesis_plus_gx_audio_eq_low | Adjust the low range band of the internal audio equalizer. |
| EQ Mid | genesis_plus_gx_audio_eq_mid | Adjust the middle range band of the internal audio equalizer. |
| EQ High | genesis_plus_gx_audio_eq_high | Adjust the high range band of the internal audio equalizer. |
| Light Gun Input | genesis_plus_gx_gun_input | Use a mouse-controlled 'Light Gun' or 'Touchscreen' input. |
| Show Light Gun Crosshair | genesis_plus_gx_gun_cursor | Display light gun crosshairs when using the MD Menacer, MD Justifiers and MS Light Phaser input device types. |
| Invert Mouse Y-Axis | genesis_plus_gx_invert_mouse | Inverts the Y-axis of the MD Mouse input device type. |
| Remove Per-Line Sprite Limit | genesis_plus_gx_no_sprite_limit | Removes the original sprite-per-scanline hardware limit. This reduces flickering but can cause visual glitches, as some games exploit the hardware limit to generate special effects. |
| Enhanced per-tile vertical scroll | genesis_plus_gx_enhanced_vscroll | Allows each individual cell to be scrolled vertically, instead of 16px 2-cell, by averaging out with the vscroll value of the neighbouring cell. This hack only applies to few games that use 2-cell vertical scroll mode. |
| Enhanced per-tile vertical scroll limit | genesis_plus_gx_enhanced_vscroll_limit | Only when Enhanced per-tile vertical scroll is enabled. Adjusts the limit of the vertical scroll enhancement. When the vscroll difference between neighbouring tiles is bigger than this limit, the enhancement is disabled. |
| CPU Speed | genesis_plus_gx_overclock | Overclock the emulated CPU. Can reduce slowdown, but may cause glitches. |
| System Lock-Ups | genesis_plus_gx_force_dtack | Emulate system lock-ups that occur on real hardware when performing illegal address access. This should only be disabled when playing certain demos and homebrew that rely on illegal behavior for correct operation. |
| 68K Address Error | genesis_plus_gx_addr_error | The Mega Drive/Genesis main CPU (Motorola 68000) generates an Address Error exception (crash) when attempting to perform unaligned memory access. Enabling this will simulate this behavior. It should only be disabled when playing ROM hacks, since the |
| CD access time | genesis_plus_gx_cd_latency | Simulate original CD hardware latency when initiating a read or seeking to a specific location on loaded disc. This is required by a few CD games that crash if CD data is available too soon and also fixes CD audio desync issues in some games. Disabl |
| PSG Tone Channel 0 Volume % | genesis_plus_gx_psg_channel_0_volume | Reduce the volume of the PSG Tone Channel 0. |
| PSG Tone Channel 1 Volume % | genesis_plus_gx_psg_channel_1_volume | Reduce the volume of the PSG Tone Channel 1. |
| PSG Tone Channel 2 Volume % | genesis_plus_gx_psg_channel_2_volume | Reduce the volume of the PSG Tone Channel 2. |
| PSG Noise Channel 3 Volume % | genesis_plus_gx_psg_channel_3_volume | Reduce the volume of the PSG Noise Channel 3. |
| Mega Drive/Genesis FM Channel 0 Volume % | genesis_plus_gx_md_channel_0_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 0. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 1 Volume % | genesis_plus_gx_md_channel_1_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 1. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 2 Volume % | genesis_plus_gx_md_channel_2_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 2. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 3 Volume % | genesis_plus_gx_md_channel_3_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 3. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 4 Volume % | genesis_plus_gx_md_channel_4_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 4. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 5 Volume % | genesis_plus_gx_md_channel_5_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 5. Only works with MAME FM emulators. |
| Master System FM (YM2413) Channel 0 Volume % | genesis_plus_gx_sms_fm_channel_0_volume | Reduce the volume of the Master System FM Channel 0. |
| Master System FM (YM2413) Channel 1 Volume % | genesis_plus_gx_sms_fm_channel_1_volume | Reduce the volume of the Master System FM Channel 1. |
| Master System FM (YM2413) Channel 2 Volume % | genesis_plus_gx_sms_fm_channel_2_volume | Reduce the volume of the Master System FM Channel 2. |
| Master System FM (YM2413) Channel 3 Volume % | genesis_plus_gx_sms_fm_channel_3_volume | Reduce the volume of the Master System FM Channel 3. |
| Master System FM (YM2413) Channel 4 Volume % | genesis_plus_gx_sms_fm_channel_4_volume | Reduce the volume of the Master System FM Channel 4. |
| Master System FM (YM2413) Channel 5 Volume % | genesis_plus_gx_sms_fm_channel_5_volume | Reduce the volume of the Master System FM Channel 5. |
| Master System FM (YM2413) Channel 6 Volume % | genesis_plus_gx_sms_fm_channel_6_volume | Reduce the volume of the Master System FM Channel 6. |
| Master System FM (YM2413) Channel 7 Volume % | genesis_plus_gx_sms_fm_channel_7_volume | Reduce the volume of the Master System FM Channel 7. |
| Master System FM (YM2413) Channel 8 Volume % | genesis_plus_gx_sms_fm_channel_8_volume | Reduce the volume of the Master System FM Channel 8. |

## SEGA Master System/Mark III

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| System | system | n/a |
| .. | .. | n/a |
| System Hardware | genesis_plus_gx_system_hw | Runs loaded content with a specific emulated console. 'Auto' will select the most appropriate system for the current game. |
| System Region | genesis_plus_gx_region_detect | Specify which region the system is from. For consoles other than the Game Gear, 'PAL' is 50 Hz, while 'NTSC' is 60 Hz. Games may run faster or slower than normal if the incorrect region is selected. |
| System Boot ROM | genesis_plus_gx_bios | Use official BIOS/bootloader for emulated hardware, if present in RetroArch's system directory. Displays console-specific start-up sequence/animation, then runs loaded content. |
| CD System BRAM (Requires Restart) | genesis_plus_gx_system_bram | When running Sega CD/Mega-CD content, specifies whether to share a single save file between all games from a specific region (Per-BIOS) or to create a separate save file for each game (Per-Game). Note that the Sega CD/Mega-CD has limited internal st |
| CD Backup Cart BRAM (Requires Restart) | genesis_plus_gx_cart_bram | When running Sega CD/Mega-CD content, specifies whether to share a single backup ram cart for all games (Per-Cart) or to create a separate backup ram cart for each game (Per-Game). |
| CD Backup Cart BRAM Size (Requires Restart) | genesis_plus_gx_cart_size | Sets the backup ram cart size when running Sega CD/Mega-CD content. Useful when setting the backup ram cart to Per-Game to avoid multiple larger cart sizes. |
| CD add-on (MD mode) (Requires Restart) | genesis_plus_gx_add_on | Specify which add-on to use for CD audio playback with supported Mega Drive/Genesis games. |
| Cartridge Lock-On | genesis_plus_gx_lock_on | Lock-On Technology is a Mega Drive/Genesis feature that allowed an older game to connect to the pass-through port of a special cartridge for extended or altered gameplay. This option specifies which type of special 'lock-on' cartridge to emulate. A  |
| Game Gear Extended Screen | genesis_plus_gx_gg_extra | Forces Game Gear titles to run in SMS mode, with an increased resolution of 256x192. May show additional content, but typically displays a border of corrupt/unwanted image data. |
| Blargg NTSC Filter | genesis_plus_gx_blargg_ntsc_filter | Apply a video filter to mimic various NTSC TV signals. |
| LCD Ghosting Filter | genesis_plus_gx_lcd_filter | Apply an image 'ghosting' filter to mimic the display characteristics of the Game Gear and Genesis Nomad LCD panels. |
| Interlaced Mode 2 Output | genesis_plus_gx_render | Interlaced Mode 2 allows the Mega Drive/Genesis to output a double height (high resolution) 320x448 image by drawing alternate scan lines each frame (this is used by Sonic the Hedgehog 2 and Combat Cars multiplayer modes). 'Double Field' mimics orig |
| Master System FM (YM2413) | genesis_plus_gx_ym2413 | Enable emulation of the FM Sound Unit used by certain Sega Mark III/Master System games for enhanced audio output. |
| Master System FM (YM2413) Core | genesis_plus_gx_ym2413_core | Select method used to emulate the FM Sound Unit of the Sega Mark III/Master System. 'MAME' option is fast, and runs full speed on most systems. 'Nuked' option is cycle accurate, very high quality, and has substantial CPU requirements. |
| Mega Drive/Genesis FM | genesis_plus_gx_ym2612 | Select method used to emulate the FM synthesizer (main sound generator) of the Mega Drive/Genesis. 'MAME' options are fast, and run full speed on most systems. 'Nuked' options are cycle accurate, very high quality, and have substantial CPU requireme |
| Sound Output | genesis_plus_gx_sound_output | Select stereo or mono sound playback. |
| Audio Filter | genesis_plus_gx_audio_filter | Enable a low pass audio filter to better simulate the characteristic sound of a Model 1 Mega Drive/Genesis. |
| Low-Pass Filter % | genesis_plus_gx_lowpass_range | Specify the cut-off frequency of the audio low pass filter. A higher value increases the perceived 'strength' of the filter, since a wider range of the high frequency spectrum is attenuated. |
| PSG Preamp Level | genesis_plus_gx_psg_preamp | Set the audio preamplifier level of the emulated SN76496 4-channel Programmable Sound Generator found in the SG-1000, Sega Mark III, Master System, Game Gear and Mega Drive/Genesis. |
| FM Preamp Level | genesis_plus_gx_fm_preamp | Set the audio preamplifier level of the emulated Mega Drive/Genesis FM sound synthesizer or Sega Mark III/Master System FM Sound Unit. |
| CD-DA Volume | genesis_plus_gx_cdda_volume | Adjust the mixing volume of the emulated CD audio playback output. |
| PCM Volume | genesis_plus_gx_pcm_volume | Adjust the mixing volume of the emulated Sega CD/Mega-CD RF5C164 PCM sound generator output. |
| EQ Low | genesis_plus_gx_audio_eq_low | Adjust the low range band of the internal audio equalizer. |
| EQ Mid | genesis_plus_gx_audio_eq_mid | Adjust the middle range band of the internal audio equalizer. |
| EQ High | genesis_plus_gx_audio_eq_high | Adjust the high range band of the internal audio equalizer. |
| Light Gun Input | genesis_plus_gx_gun_input | Use a mouse-controlled 'Light Gun' or 'Touchscreen' input. |
| Show Light Gun Crosshair | genesis_plus_gx_gun_cursor | Display light gun crosshairs when using the MD Menacer, MD Justifiers and MS Light Phaser input device types. |
| Invert Mouse Y-Axis | genesis_plus_gx_invert_mouse | Inverts the Y-axis of the MD Mouse input device type. |
| Remove Per-Line Sprite Limit | genesis_plus_gx_no_sprite_limit | Removes the original sprite-per-scanline hardware limit. This reduces flickering but can cause visual glitches, as some games exploit the hardware limit to generate special effects. |
| Enhanced per-tile vertical scroll | genesis_plus_gx_enhanced_vscroll | Allows each individual cell to be scrolled vertically, instead of 16px 2-cell, by averaging out with the vscroll value of the neighbouring cell. This hack only applies to few games that use 2-cell vertical scroll mode. |
| Enhanced per-tile vertical scroll limit | genesis_plus_gx_enhanced_vscroll_limit | Only when Enhanced per-tile vertical scroll is enabled. Adjusts the limit of the vertical scroll enhancement. When the vscroll difference between neighbouring tiles is bigger than this limit, the enhancement is disabled. |
| CPU Speed | genesis_plus_gx_overclock | Overclock the emulated CPU. Can reduce slowdown, but may cause glitches. |
| System Lock-Ups | genesis_plus_gx_force_dtack | Emulate system lock-ups that occur on real hardware when performing illegal address access. This should only be disabled when playing certain demos and homebrew that rely on illegal behavior for correct operation. |
| 68K Address Error | genesis_plus_gx_addr_error | The Mega Drive/Genesis main CPU (Motorola 68000) generates an Address Error exception (crash) when attempting to perform unaligned memory access. Enabling this will simulate this behavior. It should only be disabled when playing ROM hacks, since the |
| CD access time | genesis_plus_gx_cd_latency | Simulate original CD hardware latency when initiating a read or seeking to a specific location on loaded disc. This is required by a few CD games that crash if CD data is available too soon and also fixes CD audio desync issues in some games. Disabl |
| PSG Tone Channel 0 Volume % | genesis_plus_gx_psg_channel_0_volume | Reduce the volume of the PSG Tone Channel 0. |
| PSG Tone Channel 1 Volume % | genesis_plus_gx_psg_channel_1_volume | Reduce the volume of the PSG Tone Channel 1. |
| PSG Tone Channel 2 Volume % | genesis_plus_gx_psg_channel_2_volume | Reduce the volume of the PSG Tone Channel 2. |
| PSG Noise Channel 3 Volume % | genesis_plus_gx_psg_channel_3_volume | Reduce the volume of the PSG Noise Channel 3. |
| Mega Drive/Genesis FM Channel 0 Volume % | genesis_plus_gx_md_channel_0_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 0. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 1 Volume % | genesis_plus_gx_md_channel_1_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 1. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 2 Volume % | genesis_plus_gx_md_channel_2_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 2. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 3 Volume % | genesis_plus_gx_md_channel_3_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 3. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 4 Volume % | genesis_plus_gx_md_channel_4_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 4. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 5 Volume % | genesis_plus_gx_md_channel_5_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 5. Only works with MAME FM emulators. |
| Master System FM (YM2413) Channel 0 Volume % | genesis_plus_gx_sms_fm_channel_0_volume | Reduce the volume of the Master System FM Channel 0. |
| Master System FM (YM2413) Channel 1 Volume % | genesis_plus_gx_sms_fm_channel_1_volume | Reduce the volume of the Master System FM Channel 1. |
| Master System FM (YM2413) Channel 2 Volume % | genesis_plus_gx_sms_fm_channel_2_volume | Reduce the volume of the Master System FM Channel 2. |
| Master System FM (YM2413) Channel 3 Volume % | genesis_plus_gx_sms_fm_channel_3_volume | Reduce the volume of the Master System FM Channel 3. |
| Master System FM (YM2413) Channel 4 Volume % | genesis_plus_gx_sms_fm_channel_4_volume | Reduce the volume of the Master System FM Channel 4. |
| Master System FM (YM2413) Channel 5 Volume % | genesis_plus_gx_sms_fm_channel_5_volume | Reduce the volume of the Master System FM Channel 5. |
| Master System FM (YM2413) Channel 6 Volume % | genesis_plus_gx_sms_fm_channel_6_volume | Reduce the volume of the Master System FM Channel 6. |
| Master System FM (YM2413) Channel 7 Volume % | genesis_plus_gx_sms_fm_channel_7_volume | Reduce the volume of the Master System FM Channel 7. |
| Master System FM (YM2413) Channel 8 Volume % | genesis_plus_gx_sms_fm_channel_8_volume | Reduce the volume of the Master System FM Channel 8. |

## SEGA Megadrive/Genesis

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| System | system | n/a |
| .. | .. | n/a |
| System Hardware | genesis_plus_gx_system_hw | Runs loaded content with a specific emulated console. 'Auto' will select the most appropriate system for the current game. |
| System Region | genesis_plus_gx_region_detect | Specify which region the system is from. For consoles other than the Game Gear, 'PAL' is 50 Hz, while 'NTSC' is 60 Hz. Games may run faster or slower than normal if the incorrect region is selected. |
| System Boot ROM | genesis_plus_gx_bios | Use official BIOS/bootloader for emulated hardware, if present in RetroArch's system directory. Displays console-specific start-up sequence/animation, then runs loaded content. |
| CD System BRAM (Requires Restart) | genesis_plus_gx_system_bram | When running Sega CD/Mega-CD content, specifies whether to share a single save file between all games from a specific region (Per-BIOS) or to create a separate save file for each game (Per-Game). Note that the Sega CD/Mega-CD has limited internal st |
| CD Backup Cart BRAM (Requires Restart) | genesis_plus_gx_cart_bram | When running Sega CD/Mega-CD content, specifies whether to share a single backup ram cart for all games (Per-Cart) or to create a separate backup ram cart for each game (Per-Game). |
| CD Backup Cart BRAM Size (Requires Restart) | genesis_plus_gx_cart_size | Sets the backup ram cart size when running Sega CD/Mega-CD content. Useful when setting the backup ram cart to Per-Game to avoid multiple larger cart sizes. |
| CD add-on (MD mode) (Requires Restart) | genesis_plus_gx_add_on | Specify which add-on to use for CD audio playback with supported Mega Drive/Genesis games. |
| Cartridge Lock-On | genesis_plus_gx_lock_on | Lock-On Technology is a Mega Drive/Genesis feature that allowed an older game to connect to the pass-through port of a special cartridge for extended or altered gameplay. This option specifies which type of special 'lock-on' cartridge to emulate. A  |
| Game Gear Extended Screen | genesis_plus_gx_gg_extra | Forces Game Gear titles to run in SMS mode, with an increased resolution of 256x192. May show additional content, but typically displays a border of corrupt/unwanted image data. |
| Blargg NTSC Filter | genesis_plus_gx_blargg_ntsc_filter | Apply a video filter to mimic various NTSC TV signals. |
| LCD Ghosting Filter | genesis_plus_gx_lcd_filter | Apply an image 'ghosting' filter to mimic the display characteristics of the Game Gear and Genesis Nomad LCD panels. |
| Interlaced Mode 2 Output | genesis_plus_gx_render | Interlaced Mode 2 allows the Mega Drive/Genesis to output a double height (high resolution) 320x448 image by drawing alternate scan lines each frame (this is used by Sonic the Hedgehog 2 and Combat Cars multiplayer modes). 'Double Field' mimics orig |
| Master System FM (YM2413) | genesis_plus_gx_ym2413 | Enable emulation of the FM Sound Unit used by certain Sega Mark III/Master System games for enhanced audio output. |
| Master System FM (YM2413) Core | genesis_plus_gx_ym2413_core | Select method used to emulate the FM Sound Unit of the Sega Mark III/Master System. 'MAME' option is fast, and runs full speed on most systems. 'Nuked' option is cycle accurate, very high quality, and has substantial CPU requirements. |
| Mega Drive/Genesis FM | genesis_plus_gx_ym2612 | Select method used to emulate the FM synthesizer (main sound generator) of the Mega Drive/Genesis. 'MAME' options are fast, and run full speed on most systems. 'Nuked' options are cycle accurate, very high quality, and have substantial CPU requireme |
| Sound Output | genesis_plus_gx_sound_output | Select stereo or mono sound playback. |
| Audio Filter | genesis_plus_gx_audio_filter | Enable a low pass audio filter to better simulate the characteristic sound of a Model 1 Mega Drive/Genesis. |
| Low-Pass Filter % | genesis_plus_gx_lowpass_range | Specify the cut-off frequency of the audio low pass filter. A higher value increases the perceived 'strength' of the filter, since a wider range of the high frequency spectrum is attenuated. |
| PSG Preamp Level | genesis_plus_gx_psg_preamp | Set the audio preamplifier level of the emulated SN76496 4-channel Programmable Sound Generator found in the SG-1000, Sega Mark III, Master System, Game Gear and Mega Drive/Genesis. |
| FM Preamp Level | genesis_plus_gx_fm_preamp | Set the audio preamplifier level of the emulated Mega Drive/Genesis FM sound synthesizer or Sega Mark III/Master System FM Sound Unit. |
| CD-DA Volume | genesis_plus_gx_cdda_volume | Adjust the mixing volume of the emulated CD audio playback output. |
| PCM Volume | genesis_plus_gx_pcm_volume | Adjust the mixing volume of the emulated Sega CD/Mega-CD RF5C164 PCM sound generator output. |
| EQ Low | genesis_plus_gx_audio_eq_low | Adjust the low range band of the internal audio equalizer. |
| EQ Mid | genesis_plus_gx_audio_eq_mid | Adjust the middle range band of the internal audio equalizer. |
| EQ High | genesis_plus_gx_audio_eq_high | Adjust the high range band of the internal audio equalizer. |
| Light Gun Input | genesis_plus_gx_gun_input | Use a mouse-controlled 'Light Gun' or 'Touchscreen' input. |
| Show Light Gun Crosshair | genesis_plus_gx_gun_cursor | Display light gun crosshairs when using the MD Menacer, MD Justifiers and MS Light Phaser input device types. |
| Invert Mouse Y-Axis | genesis_plus_gx_invert_mouse | Inverts the Y-axis of the MD Mouse input device type. |
| Remove Per-Line Sprite Limit | genesis_plus_gx_no_sprite_limit | Removes the original sprite-per-scanline hardware limit. This reduces flickering but can cause visual glitches, as some games exploit the hardware limit to generate special effects. |
| Enhanced per-tile vertical scroll | genesis_plus_gx_enhanced_vscroll | Allows each individual cell to be scrolled vertically, instead of 16px 2-cell, by averaging out with the vscroll value of the neighbouring cell. This hack only applies to few games that use 2-cell vertical scroll mode. |
| Enhanced per-tile vertical scroll limit | genesis_plus_gx_enhanced_vscroll_limit | Only when Enhanced per-tile vertical scroll is enabled. Adjusts the limit of the vertical scroll enhancement. When the vscroll difference between neighbouring tiles is bigger than this limit, the enhancement is disabled. |
| CPU Speed | genesis_plus_gx_overclock | Overclock the emulated CPU. Can reduce slowdown, but may cause glitches. |
| System Lock-Ups | genesis_plus_gx_force_dtack | Emulate system lock-ups that occur on real hardware when performing illegal address access. This should only be disabled when playing certain demos and homebrew that rely on illegal behavior for correct operation. |
| 68K Address Error | genesis_plus_gx_addr_error | The Mega Drive/Genesis main CPU (Motorola 68000) generates an Address Error exception (crash) when attempting to perform unaligned memory access. Enabling this will simulate this behavior. It should only be disabled when playing ROM hacks, since the |
| CD access time | genesis_plus_gx_cd_latency | Simulate original CD hardware latency when initiating a read or seeking to a specific location on loaded disc. This is required by a few CD games that crash if CD data is available too soon and also fixes CD audio desync issues in some games. Disabl |
| PSG Tone Channel 0 Volume % | genesis_plus_gx_psg_channel_0_volume | Reduce the volume of the PSG Tone Channel 0. |
| PSG Tone Channel 1 Volume % | genesis_plus_gx_psg_channel_1_volume | Reduce the volume of the PSG Tone Channel 1. |
| PSG Tone Channel 2 Volume % | genesis_plus_gx_psg_channel_2_volume | Reduce the volume of the PSG Tone Channel 2. |
| PSG Noise Channel 3 Volume % | genesis_plus_gx_psg_channel_3_volume | Reduce the volume of the PSG Noise Channel 3. |
| Mega Drive/Genesis FM Channel 0 Volume % | genesis_plus_gx_md_channel_0_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 0. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 1 Volume % | genesis_plus_gx_md_channel_1_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 1. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 2 Volume % | genesis_plus_gx_md_channel_2_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 2. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 3 Volume % | genesis_plus_gx_md_channel_3_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 3. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 4 Volume % | genesis_plus_gx_md_channel_4_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 4. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 5 Volume % | genesis_plus_gx_md_channel_5_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 5. Only works with MAME FM emulators. |
| Master System FM (YM2413) Channel 0 Volume % | genesis_plus_gx_sms_fm_channel_0_volume | Reduce the volume of the Master System FM Channel 0. |
| Master System FM (YM2413) Channel 1 Volume % | genesis_plus_gx_sms_fm_channel_1_volume | Reduce the volume of the Master System FM Channel 1. |
| Master System FM (YM2413) Channel 2 Volume % | genesis_plus_gx_sms_fm_channel_2_volume | Reduce the volume of the Master System FM Channel 2. |
| Master System FM (YM2413) Channel 3 Volume % | genesis_plus_gx_sms_fm_channel_3_volume | Reduce the volume of the Master System FM Channel 3. |
| Master System FM (YM2413) Channel 4 Volume % | genesis_plus_gx_sms_fm_channel_4_volume | Reduce the volume of the Master System FM Channel 4. |
| Master System FM (YM2413) Channel 5 Volume % | genesis_plus_gx_sms_fm_channel_5_volume | Reduce the volume of the Master System FM Channel 5. |
| Master System FM (YM2413) Channel 6 Volume % | genesis_plus_gx_sms_fm_channel_6_volume | Reduce the volume of the Master System FM Channel 6. |
| Master System FM (YM2413) Channel 7 Volume % | genesis_plus_gx_sms_fm_channel_7_volume | Reduce the volume of the Master System FM Channel 7. |
| Master System FM (YM2413) Channel 8 Volume % | genesis_plus_gx_sms_fm_channel_8_volume | Reduce the volume of the Master System FM Channel 8. |

## SEGA Mega-CD/Sega CD

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| System | system | n/a |
| .. | .. | n/a |
| System Hardware | genesis_plus_gx_system_hw | Runs loaded content with a specific emulated console. 'Auto' will select the most appropriate system for the current game. |
| System Region | genesis_plus_gx_region_detect | Specify which region the system is from. For consoles other than the Game Gear, 'PAL' is 50 Hz, while 'NTSC' is 60 Hz. Games may run faster or slower than normal if the incorrect region is selected. |
| System Boot ROM | genesis_plus_gx_bios | Use official BIOS/bootloader for emulated hardware, if present in RetroArch's system directory. Displays console-specific start-up sequence/animation, then runs loaded content. |
| CD System BRAM (Requires Restart) | genesis_plus_gx_system_bram | When running Sega CD/Mega-CD content, specifies whether to share a single save file between all games from a specific region (Per-BIOS) or to create a separate save file for each game (Per-Game). Note that the Sega CD/Mega-CD has limited internal st |
| CD Backup Cart BRAM (Requires Restart) | genesis_plus_gx_cart_bram | When running Sega CD/Mega-CD content, specifies whether to share a single backup ram cart for all games (Per-Cart) or to create a separate backup ram cart for each game (Per-Game). |
| CD Backup Cart BRAM Size (Requires Restart) | genesis_plus_gx_cart_size | Sets the backup ram cart size when running Sega CD/Mega-CD content. Useful when setting the backup ram cart to Per-Game to avoid multiple larger cart sizes. |
| CD add-on (MD mode) (Requires Restart) | genesis_plus_gx_add_on | Specify which add-on to use for CD audio playback with supported Mega Drive/Genesis games. |
| Cartridge Lock-On | genesis_plus_gx_lock_on | Lock-On Technology is a Mega Drive/Genesis feature that allowed an older game to connect to the pass-through port of a special cartridge for extended or altered gameplay. This option specifies which type of special 'lock-on' cartridge to emulate. A  |
| Game Gear Extended Screen | genesis_plus_gx_gg_extra | Forces Game Gear titles to run in SMS mode, with an increased resolution of 256x192. May show additional content, but typically displays a border of corrupt/unwanted image data. |
| Blargg NTSC Filter | genesis_plus_gx_blargg_ntsc_filter | Apply a video filter to mimic various NTSC TV signals. |
| LCD Ghosting Filter | genesis_plus_gx_lcd_filter | Apply an image 'ghosting' filter to mimic the display characteristics of the Game Gear and Genesis Nomad LCD panels. |
| Interlaced Mode 2 Output | genesis_plus_gx_render | Interlaced Mode 2 allows the Mega Drive/Genesis to output a double height (high resolution) 320x448 image by drawing alternate scan lines each frame (this is used by Sonic the Hedgehog 2 and Combat Cars multiplayer modes). 'Double Field' mimics orig |
| Master System FM (YM2413) | genesis_plus_gx_ym2413 | Enable emulation of the FM Sound Unit used by certain Sega Mark III/Master System games for enhanced audio output. |
| Master System FM (YM2413) Core | genesis_plus_gx_ym2413_core | Select method used to emulate the FM Sound Unit of the Sega Mark III/Master System. 'MAME' option is fast, and runs full speed on most systems. 'Nuked' option is cycle accurate, very high quality, and has substantial CPU requirements. |
| Mega Drive/Genesis FM | genesis_plus_gx_ym2612 | Select method used to emulate the FM synthesizer (main sound generator) of the Mega Drive/Genesis. 'MAME' options are fast, and run full speed on most systems. 'Nuked' options are cycle accurate, very high quality, and have substantial CPU requireme |
| Sound Output | genesis_plus_gx_sound_output | Select stereo or mono sound playback. |
| Audio Filter | genesis_plus_gx_audio_filter | Enable a low pass audio filter to better simulate the characteristic sound of a Model 1 Mega Drive/Genesis. |
| Low-Pass Filter % | genesis_plus_gx_lowpass_range | Specify the cut-off frequency of the audio low pass filter. A higher value increases the perceived 'strength' of the filter, since a wider range of the high frequency spectrum is attenuated. |
| PSG Preamp Level | genesis_plus_gx_psg_preamp | Set the audio preamplifier level of the emulated SN76496 4-channel Programmable Sound Generator found in the SG-1000, Sega Mark III, Master System, Game Gear and Mega Drive/Genesis. |
| FM Preamp Level | genesis_plus_gx_fm_preamp | Set the audio preamplifier level of the emulated Mega Drive/Genesis FM sound synthesizer or Sega Mark III/Master System FM Sound Unit. |
| CD-DA Volume | genesis_plus_gx_cdda_volume | Adjust the mixing volume of the emulated CD audio playback output. |
| PCM Volume | genesis_plus_gx_pcm_volume | Adjust the mixing volume of the emulated Sega CD/Mega-CD RF5C164 PCM sound generator output. |
| EQ Low | genesis_plus_gx_audio_eq_low | Adjust the low range band of the internal audio equalizer. |
| EQ Mid | genesis_plus_gx_audio_eq_mid | Adjust the middle range band of the internal audio equalizer. |
| EQ High | genesis_plus_gx_audio_eq_high | Adjust the high range band of the internal audio equalizer. |
| Light Gun Input | genesis_plus_gx_gun_input | Use a mouse-controlled 'Light Gun' or 'Touchscreen' input. |
| Show Light Gun Crosshair | genesis_plus_gx_gun_cursor | Display light gun crosshairs when using the MD Menacer, MD Justifiers and MS Light Phaser input device types. |
| Invert Mouse Y-Axis | genesis_plus_gx_invert_mouse | Inverts the Y-axis of the MD Mouse input device type. |
| Remove Per-Line Sprite Limit | genesis_plus_gx_no_sprite_limit | Removes the original sprite-per-scanline hardware limit. This reduces flickering but can cause visual glitches, as some games exploit the hardware limit to generate special effects. |
| Enhanced per-tile vertical scroll | genesis_plus_gx_enhanced_vscroll | Allows each individual cell to be scrolled vertically, instead of 16px 2-cell, by averaging out with the vscroll value of the neighbouring cell. This hack only applies to few games that use 2-cell vertical scroll mode. |
| Enhanced per-tile vertical scroll limit | genesis_plus_gx_enhanced_vscroll_limit | Only when Enhanced per-tile vertical scroll is enabled. Adjusts the limit of the vertical scroll enhancement. When the vscroll difference between neighbouring tiles is bigger than this limit, the enhancement is disabled. |
| CPU Speed | genesis_plus_gx_overclock | Overclock the emulated CPU. Can reduce slowdown, but may cause glitches. |
| System Lock-Ups | genesis_plus_gx_force_dtack | Emulate system lock-ups that occur on real hardware when performing illegal address access. This should only be disabled when playing certain demos and homebrew that rely on illegal behavior for correct operation. |
| 68K Address Error | genesis_plus_gx_addr_error | The Mega Drive/Genesis main CPU (Motorola 68000) generates an Address Error exception (crash) when attempting to perform unaligned memory access. Enabling this will simulate this behavior. It should only be disabled when playing ROM hacks, since the |
| CD access time | genesis_plus_gx_cd_latency | Simulate original CD hardware latency when initiating a read or seeking to a specific location on loaded disc. This is required by a few CD games that crash if CD data is available too soon and also fixes CD audio desync issues in some games. Disabl |
| PSG Tone Channel 0 Volume % | genesis_plus_gx_psg_channel_0_volume | Reduce the volume of the PSG Tone Channel 0. |
| PSG Tone Channel 1 Volume % | genesis_plus_gx_psg_channel_1_volume | Reduce the volume of the PSG Tone Channel 1. |
| PSG Tone Channel 2 Volume % | genesis_plus_gx_psg_channel_2_volume | Reduce the volume of the PSG Tone Channel 2. |
| PSG Noise Channel 3 Volume % | genesis_plus_gx_psg_channel_3_volume | Reduce the volume of the PSG Noise Channel 3. |
| Mega Drive/Genesis FM Channel 0 Volume % | genesis_plus_gx_md_channel_0_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 0. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 1 Volume % | genesis_plus_gx_md_channel_1_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 1. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 2 Volume % | genesis_plus_gx_md_channel_2_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 2. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 3 Volume % | genesis_plus_gx_md_channel_3_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 3. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 4 Volume % | genesis_plus_gx_md_channel_4_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 4. Only works with MAME FM emulators. |
| Mega Drive/Genesis FM Channel 5 Volume % | genesis_plus_gx_md_channel_5_volume | Reduce the volume of the Mega Drive/Genesis FM Channel 5. Only works with MAME FM emulators. |
| Master System FM (YM2413) Channel 0 Volume % | genesis_plus_gx_sms_fm_channel_0_volume | Reduce the volume of the Master System FM Channel 0. |
| Master System FM (YM2413) Channel 1 Volume % | genesis_plus_gx_sms_fm_channel_1_volume | Reduce the volume of the Master System FM Channel 1. |
| Master System FM (YM2413) Channel 2 Volume % | genesis_plus_gx_sms_fm_channel_2_volume | Reduce the volume of the Master System FM Channel 2. |
| Master System FM (YM2413) Channel 3 Volume % | genesis_plus_gx_sms_fm_channel_3_volume | Reduce the volume of the Master System FM Channel 3. |
| Master System FM (YM2413) Channel 4 Volume % | genesis_plus_gx_sms_fm_channel_4_volume | Reduce the volume of the Master System FM Channel 4. |
| Master System FM (YM2413) Channel 5 Volume % | genesis_plus_gx_sms_fm_channel_5_volume | Reduce the volume of the Master System FM Channel 5. |
| Master System FM (YM2413) Channel 6 Volume % | genesis_plus_gx_sms_fm_channel_6_volume | Reduce the volume of the Master System FM Channel 6. |
| Master System FM (YM2413) Channel 7 Volume % | genesis_plus_gx_sms_fm_channel_7_volume | Reduce the volume of the Master System FM Channel 7. |
| Master System FM (YM2413) Channel 8 Volume % | genesis_plus_gx_sms_fm_channel_8_volume | Reduce the volume of the Master System FM Channel 8. |

## SEGA Megadrive 32X/Sega 32X

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| System Region | picodrive_region | Specify which region the system is from. 'PAL'/'Europe' is 50hz while 'NTSC'/'US' is 60hz. Games may run faster or slower than normal (or produce errors) if the incorrect region is selected. |
| Master System Type | picodrive_smstype | Choose which type of hardware (SMS or Game Gear) the core should emulate when running Master System content. |
| Master System ROM Mapping | picodrive_smsmapper | Choose which ROM mapper the core should apply. 'Auto' will work for a wide range of content, but in some cases automatic detection fails. |
| Sega CD RAM Cart | picodrive_ramcart | Emulate a Sega CD RAM cart, used for save game data. WARNING: When enabled, internal save data (BRAM) will be discarded. |
| Video Renderer | picodrive_renderer | Specify video rendering method. 'Accurate' is slowest, but most exact. 'Good' is faster, but fails if colors change mid-frame too often. 'Fast' renders the complete frame in one pass, and is incompatible with games that rely on mid-frame palette/spr |
| Audio Sample Rate (Hz) | picodrive_sound_rate | Higher values increase sound quality. Lower values may increase performance. Native is the Megadrive sound chip rate (~53000). Select this if you want the most accurate audio. |
| FM filtering | picodrive_fm_filter | Enable filtering for Mega Drive FM sound at non-native bitrates. Sound output will improve, at the price of being noticeably slower |
| Master System FM Sound Unit | picodrive_smsfm | Enable emulation of the SMS FM Sound Unit. This produces higher quality audio in some games, but non-Japanese titles may fail to run. |
| Mega Drive FM DAC noise | picodrive_dacnoise | Enable emulation of YM2612 DAC noise. This option generates a distortion which existed on most Model 1 Mega Drive/Genesis, but not on newer models. |
| Audio Filter | picodrive_audio_filter | Enable a low pass audio filter to better simulate the characteristic sound of a Model 1 Mega Drive/Genesis. Note that only Model 1 and its add-ons (Sega CD, 32X) employed a physical low pass filter. |
| Low-Pass Filter % | picodrive_lowpass_range | Specify the cut-off frequency of the low pass audio filter. A higher value increases the perceived 'strength' of the filter, since a wider range of the high frequency spectrum is attenuated. |
| Input Device 1 | picodrive_input1 | Choose which type of controller is plugged into slot 1. Note that a multiplayer adaptor uses both slots. |
| Input Device 2 | picodrive_input2 | Choose which type of controller is plugged into slot 2. This setting is ignored when a multiplayer adaptor is plugged into slot 1. |
| Dynamic Recompilers | picodrive_drc | Enable dynamic recompilers which help to improve performance. Less accurate than interpreter CPU cores, but significantly faster. |
| No Sprite Limit | picodrive_sprlim | Removes the original sprite-per-scanline hardware limit. This reduces flickering but can cause visual glitches, as some games exploit the hardware limit to generate special effects. |
| 68K Overclock | picodrive_overclk68k | Overclock the emulated 68K chip. Can reduce slowdown, but may cause glitches. |

## SEGA Saturn

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| System Region | beetle_saturn_region | Choose which region the system is from. |
| BIOS language | beetle_saturn_autortc_lang | Also affects language used in some games (e.g. the European release of 'Panzer Dragoon'). |
| CD Image Cache (Restart) | beetle_saturn_cdimagecache | Loads the complete image in memory at startup. Can potentially decrease loading times at the cost of increased startup time. Requires a restart in order for a change to take effect. |
| Mid-frame Input Synchronization | beetle_saturn_midsync | Mid-frame synchronization can reduce input latency, but it will increase CPU requirements. |
| Automatically set RTC on game load | beetle_saturn_autortc | Automatically set the SMPC's emulated Real-Time Clock to the host system's current time and date upon game load. |
| Enable Horizontal Blend(blur) | beetle_saturn_horizontal_blend | Enable horizontal blend(blur) filter. Has a more noticeable effect with the Saturn's higher horizontal resolution modes(640/704). |
| 6Player Adaptor on Port 1 | beetle_saturn_multitap_port1 | Enable multitap on Saturn port 1. |
| 6Player Adaptor on Port 2 | beetle_saturn_multitap_port2 | Enable multitap on Saturn port 2. |
| Allow Up+Down and Left+Right | beetle_saturn_opposite_directions | Enabling this will allow pressing up and down or left and right directions at the same time. This may cause glitches. |
| Analog Stick Deadzone | beetle_saturn_analog_stick_deadzone | Configure the '3D Control Pad' Device Type's analog deadzone. |
| Trigger Deadzone | beetle_saturn_trigger_deadzone | Configure the '3D Control Pad' Device Type's trigger deadzone. |
| Mouse Sensitivity | beetle_saturn_mouse_sensitivity | Configure the 'Mouse' device type's sensitivity. |
| Gun Crosshair | beetle_saturn_virtuagun_crosshair | Choose the crosshair for the 'Stunner' and 'Virtua Gun' device types. Setting it to Off disables the crosshair. |
| Gun Input Mode | beetle_saturn_virtuagun_input | n/a |
| Cartridge | beetle_saturn_cart | Certain games require an external cartridge to run (ROM Cart, 1M RAM Cart, 4M RAM Cart). |
| Shared Internal Memory (Restart) | beetle_saturn_shared_int | Enables shared internal memory. |
| Shared Backup Memory (Restart) | beetle_saturn_shared_ext | Enables shared backup memory. |

## SEGA Dreamcast

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Region | reicast_region | n/a |
| Language | reicast_language | Changes the language used by the BIOS and by any games that contain multiple languages. |
| HLE BIOS (Restart Required) | reicast_hle_bios | Force use of high-level emulation BIOS. |
| Boot to BIOS (Restart Required) | reicast_boot_to_bios | Boot directly into the Dreamcast BIOS menu. |
| Enable DSP | reicast_enable_dsp | Enable emulation of the Dreamcast's audio DSP (digital signal processor). Improves the accuracy of generated sound, but increases performance requirements. |
| Force Windows CE Mode | reicast_force_wince | Enable full MMU (Memory Management Unit) emulation and other settings for Windows CE games. |
| Allow NAOMI Service Buttons | reicast_allow_service_buttons | Enables SERVICE button for NAOMI, to enter cabinet settings. |
| Set NAOMI Games to Free Play | reicast_force_freeplay | Modify to coin settings of the game to free play. |
| Broadband Adapter Emulation | reicast_emulate_bba | Emulate the ethernet broadband adapter instead of the modem. (Restart Required) |
| Enable UPnP | reicast_upnp | Use UPnP to automatically configure your Internet router for online games. |
| Cable Type | reicast_cable_type | The output signal type. 'TV (Composite)' is the most widely supported. |
| Broadcast Standard | reicast_broadcast | n/a |
| Screen Orientation | reicast_screen_rotation | n/a |
| Alpha Sorting | reicast_alpha_sorting | n/a |
| Full framebuffer emulation | reicast_emulate_framebuffer | Enable full framebuffer emulation in VRAM. This is useful for games that directly read or write the framebuffer in VRAM. When enabled, Internal Resolution is forced to 640x480 and performance may be severely impacted. |
| Enable RTT (Render To Texture) Buffer | reicast_enable_rttb | Copy rendered textures back from the GPU to VRAM. This option is normally enabled for games that require it. When enabled, texture rendering upscaling is disabled and performance may be impacted. |
| Mipmapping | reicast_mipmapping | n/a |
| Fog Effects | reicast_fog | n/a |
| Volume Modifier | reicast_volume_modifier_enable | A Dreamcast GPU feature that is typically used by games to draw object shadows. This should normally be enabled - the performance impact is usually minimal to negligible. |
| Anisotropic Filtering | reicast_anisotropic_filtering | Enhance the quality of textures on surfaces that are at oblique viewing angles with respect to the camera. Higher values are more demanding on the GPU. Changes to this setting only apply after restarting. |
| Texture Filtering | reicast_texture_filtering | The texture filtering mode to use. This can be used to force a certain texture filtering mode on all textures to get a crisper (or smoother) appearance than Default. Values other than Default may cause various rendering issues. Changes to this setti |
| Delay Frame Swapping | reicast_delay_frame_swapping | Useful to avoid flashing screens or glitchy videos. Not recommended on slow platforms. |
| Detect Frame Rate Changes | reicast_detect_vsync_swap_interval | Notify frontend when internal frame rate changes (e.g. from 60 fps to 30 fps). Improves frame pacing in games that run at a locked 30 fps or 20 fps, but should be disabled for games with unlocked (unstable) frame rates (e.g. Ecco the Dolphin, Unreal |
| Native Depth Interpolation | reicast_native_depth_interpolation | Helps with texture corruption and depth issues on AMD GPUs. Can also help Intel GPUs in some cases. |
| Threaded Rendering | reicast_threaded_rendering | Runs the GPU and CPU on different threads. Highly recommended. |
| GD-ROM Fast Loading (inaccurate) | reicast_gdrom_fast_loading | Speeds up GD-ROM loading. |
| Dreamcast 32MB RAM Mod | reicast_dc_32mb_mod | Enables 32MB RAM Mod for Dreamcast. May affect compatibility |
| SH4 CPU under/overclock | reicast_sh4clock | Change the SH4 main CPU clock from the default 200 MHz. Underclocking may help slow platforms. Overclocking may increase the frame rate for some games. Use with caution. |
| Analog Stick Deadzone | reicast_analog_stick_deadzone | n/a |
| Trigger Deadzone | reicast_trigger_deadzone | n/a |
| Digital Triggers | reicast_digital_triggers | n/a |
| Purupuru Pack/Vibration Pack | reicast_enable_purupuru | Enables controller force feedback. |
| Broadcast Digital Outputs | reicast_network_output | Broadcast digital outputs and force-feedback state on TCP port 8000. Compatible with the "-output network" MAME option. |
| Show Light Gun Settings | reicast_show_lightgun_settings | Enable configuration of light gun crosshair display options. NOTE: Quick Menu may need to be toggled for this setting to take effect. |
| Gun Crosshair Size Scaling | reicast_lightgun_crosshair_size_scaling | n/a |
| Gun Crosshair 1 Display | reicast_lightgun1_crosshair | n/a |
| Gun Crosshair 2 Display | reicast_lightgun2_crosshair | n/a |
| Gun Crosshair 3 Display | reicast_lightgun3_crosshair | n/a |
| Gun Crosshair 4 Display | reicast_lightgun4_crosshair | n/a |
| Per-Game Visual Memory Units/Systems (VMU) | reicast_per_content_vmus | When disabled, all games share 4 VMU save files (A1, B1, C1, D1) located in RetroArch's system directory. The 'VMU A1' setting creates a unique VMU 'A1' file in RetroArch's save directory for each game that is launched. The 'All VMUs' setting create |
| Visual Memory Units/Systems (VMU) Sounds | reicast_vmu_sound | When enabled, VMU beeps are played. |
| Show Visual Memory Unit/System (VMU) Display Settings | reicast_show_vmu_screen_settings | Enable configuration of emulated VMU LCD screen visibility, size, position and color. NOTE: Quick Menu may need to be toggled for this setting to take effect. |
| VMU Screen 1 Display | reicast_vmu1_screen_display | n/a |
| VMU Screen 1 Position | reicast_vmu1_screen_position | n/a |
| VMU Screen 1 Size | reicast_vmu1_screen_size_mult | n/a |
| VMU Screen 1 Pixel On Color | reicast_vmu1_pixel_on_color | n/a |
| VMU Screen 1 Pixel Off Color | reicast_vmu1_pixel_off_color | n/a |
| VMU Screen 1 Opacity | reicast_vmu1_screen_opacity | n/a |
| VMU Screen 2 Display | reicast_vmu2_screen_display | n/a |
| VMU Screen 2 Position | reicast_vmu2_screen_position | n/a |
| VMU Screen 2 Size | reicast_vmu2_screen_size_mult | n/a |
| VMU Screen 2 Pixel On Color | reicast_vmu2_pixel_on_color | n/a |
| VMU Screen 2 Pixel Off Color | reicast_vmu2_pixel_off_color | n/a |
| VMU Screen 2 Opacity | reicast_vmu2_screen_opacity | n/a |
| VMU Screen 3 Display | reicast_vmu3_screen_display | n/a |
| VMU Screen 3 Position | reicast_vmu3_screen_position | n/a |
| VMU Screen 3 Size | reicast_vmu3_screen_size_mult | n/a |
| VMU Screen 3 Pixel On Color | reicast_vmu3_pixel_on_color | n/a |
| VMU Screen 3 Pixel Off Color | reicast_vmu3_pixel_off_color | n/a |
| VMU Screen 3 Opacity | reicast_vmu3_screen_opacity | n/a |
| VMU Screen 4 Display | reicast_vmu4_screen_display | n/a |
| VMU Screen 4 Position | reicast_vmu4_screen_position | n/a |
| VMU Screen 4 Size | reicast_vmu4_screen_size_mult | n/a |
| VMU Screen 4 Pixel On Color | reicast_vmu4_pixel_on_color | n/a |
| VMU Screen 4 Pixel Off Color | reicast_vmu4_pixel_off_color | n/a |
| VMU Screen 4 Opacity | reicast_vmu4_screen_opacity | n/a |

## SNK NEO-GEO (AES/MVS)

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Vertical mode | fbneo-vertical-mode | Rotate display for vertical screens |
| Force 60Hz | fbneo-force-60hz | Ignore game's original refresh rate and try to run it at 60hz instead. It will cause incorrect game speed and frame pacing. It will try to use your monitor's correct refresh rate instead of 60hz if this refresh rate is between 59hz and 61hz. |
| Allow patched romsets | fbneo-allow-patched-romsets | Allow romsets from your system/fbneo/patched/ folder to override your romsets, crcs will be ignored but sizes and names must still match, you need to close content for this setting to take effect |
| Analog Speed | fbneo-analog-speed | Mitigate analog controls speed, some games might require low values to be playable |
| Crosshair emulation | fbneo-lightgun-crosshair-emulation | Change emulated crosshair behavior |
| CPU clock | fbneo-cpu-speed-adjust | Change emulated cpu frequency for various systems, by increasing you can fix native slowdowns in some games, by decreasing you can help performance on low-end devices |
| Diagnostic Input | fbneo-diagnostic-input | Configure button combination to enter cabinet service menu |
| Neo-Geo mode | fbneo-neogeo-mode | Load appropriate bios depending on your choice, under the condition such a bios is compatible with the running game |
| Memory card mode | fbneo-memcard-mode | Change the behavior for the memory card |
| Debug Dip 1_1 | fbneo-debug-dip-1-1 | Enable Debug Dip 1_1 |
| Debug Dip 1_2 | fbneo-debug-dip-1-2 | Enable Debug Dip 1_2 |
| Debug Dip 1_3 | fbneo-debug-dip-1-3 | Enable Debug Dip 1_3 |
| Debug Dip 1_4 | fbneo-debug-dip-1-4 | Enable Debug Dip 1_4 |
| Debug Dip 1_5 | fbneo-debug-dip-1-5 | Enable Debug Dip 1_5 |
| Debug Dip 1_6 | fbneo-debug-dip-1-6 | Enable Debug Dip 1_6 |
| Debug Dip 1_7 | fbneo-debug-dip-1-7 | Enable Debug Dip 1_7 |
| Debug Dip 1_8 | fbneo-debug-dip-1-8 | Enable Debug Dip 1_8 |
| Debug Dip 2_1 | fbneo-debug-dip-2-1 | Enable Debug Dip 2_1 |
| Debug Dip 2_2 | fbneo-debug-dip-2-2 | Enable Debug Dip 2_2 |
| Debug Dip 2_3 | fbneo-debug-dip-2-3 | Enable Debug Dip 2_3 |
| Debug Dip 2_4 | fbneo-debug-dip-2-4 | Enable Debug Dip 2_4 |
| Debug Dip 2_5 | fbneo-debug-dip-2-5 | Enable Debug Dip 2_5 |
| Debug Dip 2_6 | fbneo-debug-dip-2-6 | Enable Debug Dip 2_6 |
| Debug Dip 2_7 | fbneo-debug-dip-2-7 | Enable Debug Dip 2_7 |
| Debug Dip 2_8 | fbneo-debug-dip-2-8 | Enable Debug Dip 2_8 |
| Samplerate | fbneo-samplerate | Configure samplerate, it could impact performances, closing & starting game again is required |
| Sample Interpolation | fbneo-sample-interpolation | Configure sample interpolation, it could impact performances |
| FM Interpolation | fbneo-fm-interpolation | Configure FM interpolation, it could impact performances |
| LowPass Filter | fbneo-lowpass-filter | Enable LowPass Filter |
| [Dipswitch] Autofire | fbneo-dipswitch-bstars-Autofire | Dipswitch setting, setting is specific to the running romset. Some dipswitches require a restart to work properly. |
| [Dipswitch] Setting mode | fbneo-dipswitch-bstars-Setting_mode | Dipswitch setting, setting is specific to the running romset. Some dipswitches require a restart to work properly. |
| [Dipswitch] Coin chutes | fbneo-dipswitch-bstars-Coin_chutes | Dipswitch setting, setting is specific to the running romset. Some dipswitches require a restart to work properly. |
| [Dipswitch] Coin chutes | fbneo-dipswitch-bstars-Coin_chutes_2 | Dipswitch setting, setting is specific to the running romset. Some dipswitches require a restart to work properly. |
| [Dipswitch] Commmunicaton | fbneo-dipswitch-bstars-Commmunicaton | Dipswitch setting, setting is specific to the running romset. Some dipswitches require a restart to work properly. |
| [Dipswitch] Free play | fbneo-dipswitch-bstars-Free_play | Dipswitch setting, setting is specific to the running romset. Some dipswitches require a restart to work properly. |
| [Dipswitch] Stop mode | fbneo-dipswitch-bstars-Stop_mode | Dipswitch setting, setting is specific to the running romset. Some dipswitches require a restart to work properly. |
| [Dipswitch] BIOS | fbneo-dipswitch-bstars-BIOS | Dipswitch setting, setting is specific to the running romset. Some dipswitches require a restart to work properly. |
| [Dipswitch] Memory card | fbneo-dipswitch-bstars-Memory_card | Dipswitch setting, setting is specific to the running romset. Some dipswitches require a restart to work properly. |
| [Dipswitch] New card type | fbneo-dipswitch-bstars-New_card_type | Dipswitch setting, setting is specific to the running romset. Some dipswitches require a restart to work properly. |

## SNK NEO-GEO CD

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Vertical mode | fbneo-vertical-mode | Rotate display for vertical screens |
| Force 60Hz | fbneo-force-60hz | Ignore game's original refresh rate and try to run it at 60hz instead. It will cause incorrect game speed and frame pacing. It will try to use your monitor's correct refresh rate instead of 60hz if this refresh rate is between 59hz and 61hz. |
| Allow patched romsets | fbneo-allow-patched-romsets | Allow romsets from your system/fbneo/patched/ folder to override your romsets, crcs will be ignored but sizes and names must still match, you need to close content for this setting to take effect |
| Analog Speed | fbneo-analog-speed | Mitigate analog controls speed, some games might require low values to be playable |
| Crosshair emulation | fbneo-lightgun-crosshair-emulation | Change emulated crosshair behavior |
| CPU clock | fbneo-cpu-speed-adjust | Change emulated cpu frequency for various systems, by increasing you can fix native slowdowns in some games, by decreasing you can help performance on low-end devices |
| Diagnostic Input | fbneo-diagnostic-input | Configure button combination to enter cabinet service menu |
| Sample Interpolation | fbneo-sample-interpolation | Configure sample interpolation, it could impact performances |
| FM Interpolation | fbneo-fm-interpolation | Configure FM interpolation, it could impact performances |
| LowPass Filter | fbneo-lowpass-filter | Enable LowPass Filter |
| [Dipswitch] Region | fbneo-dipswitch-neocdz-Region | Dipswitch setting, setting is specific to the running romset. Some dipswitches require a restart to work properly. |
| [Dipswitch] BIOS | fbneo-dipswitch-neocdz-BIOS | Dipswitch setting, setting is specific to the running romset. Some dipswitches require a restart to work properly. |
| [Dipswitch] CD Loading Speed | fbneo-dipswitch-neocdz-CD_Loading_Speed | Dipswitch setting, setting is specific to the running romset. Some dipswitches require a restart to work properly. |

## SNK NEO-GEO Pocket

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Language (*) | ngp_language | n/a |

## SONY PlayStation

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| **Raspberry Pi 4 and higher** {: colspan=3} |
| Console Region | swanstation_Console_Region | Determines which region/hardware to emulate. Auto-Detect will use the region of the disc inserted. |
| NTSC-J BIOS (Restart) | swanstation_BIOS_PathNTSCJ | Select which standard BIOS to use for NTSC-J. |
| NTSC-U BIOS (Restart) | swanstation_BIOS_PathNTSCU | Select which standard BIOS to use for NTSC-U. |
| PAL BIOS (Restart) | swanstation_BIOS_PathPAL | Select which standard BIOS to use for PAL. |
| Fast Boot | swanstation_BIOS_PatchFastBoot | Skips the BIOS shell/intro, booting directly into the game. Usually safe to enable, but some games break. |
| CD-ROM Region Check | swanstation_CDROM_RegionCheck | Prevents discs from incorrect regions being read by the emulator. Usually safe to disable. |
| CD-ROM Read Thread | swanstation_CDROM_ReadThread | Reads CD-ROM sectors ahead asynchronously, reducing the risk of frame time spikes. |
| Apply Image Patches (Restart) | swanstation_CDROM_LoadImagePatches | Automatically applies patches to disc images when they are present in the same directory. Currently only PPF patches are supported with this option. Requires the core to be restarted to apply. |
| Preload CD-ROM Image To RAM | swanstation_CDROM_LoadImageToRAM | Loads the disc image to RAM before starting emulation. May reduce hitching if you are running off a network share, at a cost of a greater startup time. As libretro provides no way to draw overlays, the emulator will appear to lock up while the image |
| Pre-cache CHD Images To RAM | swanstation_CDROM_PreCacheCHD | Pre-caches CHD CD-ROM images to RAM without decompressing them. Unlike the preload option, this option supports M3U files. It is also faster and requires less RAM compared to preloading as it doesn't decompress the CHD. |
| Mute CD Audio | swanstation_CDROM_MuteCDAudio | Forcibly mutes both CD-DA and XA audio from the CD-ROM. Can be used to disable background music in some games. |
| CD-ROM Read Speedup | swanstation_CDROM_ReadSpeedup | Speeds up CD-ROM reads by the specified factor. Only applies to double-speed reads, and is ignored when audio is playing. May improve loading speeds in some games, at the cost of breaking others. |
| CD-ROM Seek Speedup | swanstation_CDROM_SeekSpeedup | Speeds up CD-ROM seeks by the specified factor. May improve loading speeds in some game, at the cost of breaking others. |
| CPU Execution Mode | swanstation_CPU_ExecutionMode | Which mode to use for CPU emulation. Recompiler provides the best performance. |
| GPU Renderer | swanstation_GPU_Renderer | Which renderer to use to emulate the GPU. |
| Threaded Rendering (Software) | swanstation_GPU_UseThread | Uses a second thread for drawing graphics. Currently only available for the software renderer. |
| Use Software Renderer For Readbacks (Restart) | swanstation_GPU_UseSoftwareRendererForReadbacks | Runs the software renderer in parallel for VRAM readbacks. Some games may require this to be enabled to produce proper framebuffer effects (e.g. motion blur, battle swirls ect.), or otherwise fix corrupted textures when using the hardware renderers. |
| True Color Rendering | swanstation_GPU_TrueColor | Disables dithering and uses the full 8 bits per channel of color information. May break rendering in some games. |
| Disable Interlacing | swanstation_GPU_DisableInterlacing | Disables interlaced rendering and display in the GPU. Some games can render in 480p this way, but others will break. |
| Force NTSC Timings | swanstation_GPU_ForceNTSCTimings | Forces PAL games to run at NTSC timings, i.e. 60hz. Some PAL games will run at their "normal" speeds, while others will break. |
| Force 4:3 For 24-Bit Display | swanstation_Display_Force4_3For24Bit | Switches back to 4:3 display aspect ratio when displaying 24-bit content, usually FMVs. |
| Chroma Smoothing For 24-Bit Display | swanstation_GPU_ChromaSmoothing24Bit | Smooths out blockyness between colour transitions in 24-bit content, usually FMVs. Only applies to the hardware renderers. |
| PGXP Geometry Correction | swanstation_GPU_PGXPEnable | Reduces "wobbly" polygons by attempting to preserve the fractional component through memory transfers. Only works with the hardware renderers, and may not be compatible with all games. |
| PGXP Culling Correction | swanstation_GPU_PGXPCulling | Increases the precision of polygon culling, reducing the number of holes in geometry. Requires geometry correction enabled. |
| PGXP Perspective Correct Textures | swanstation_GPU_PGXPTextureCorrection | Uses perspective-correct interpolation for texture coordinates, straightening out warped textures. Requires geometry correction enabled. |
| PGXP Perspective Correct Colors | swanstation_GPU_PGXPColorCorrection | Uses perspective-correct interpolation for vertex colors, which can improve visuals in some games, but cause rendering errors in others. Requires geometry correction enabled. |
| PGXP Depth Buffer | swanstation_GPU_PGXPDepthBuffer | Attempts to reduce polygon Z-fighting by testing pixels against the depth values from PGXP. Low compatibility, but can work well in some games. Requires geometry correction enabled. |
| PGXP Vertex Cache | swanstation_GPU_PGXPVertexCache | Uses screen coordinates as a fallback when tracking vertices through memory fails. May improve PGXP compatibility. |
| PGXP CPU Mode | swanstation_GPU_PGXPCPU | Tries to track vertex manipulation through the CPU. Some games require this option for PGXP to be effective. Very slow, and incompatible with the recompiler. |
| PGXP Preserve Projection Precision | swanstation_GPU_PGXPPreserveProjFP | Enables additional precision for PGXP. May improve visuals in some games but break others. |
| PGXP Geometry Tolerance | swanstation_GPU_PGXPTolerance | Ignores precise positions if the difference exceeds this threshold. |
| PGXP Depth Clear Threshold | swanstation_GPU_PGXPDepthClearThreshold | Sets the threshold for the PGXP Depth Buffer. |
| Display OSD Messages | swanstation_Display_ShowOSDMessages | Shows on-screen messages generated by the core. |
| Memory Card 1 Type (Restart) | swanstation_MemoryCards_Card1Type | Sets the type of memory card for Slot 1. Restart the core when switching formats. 'Shared Between All Games' and both 'Separate Card Per Game' options may be used for legacy purposes, and are unsupported. 'Libretro' (.srm) and 'Separate Card Per Gam |
| Memory Card 2 Type | swanstation_MemoryCards_Card2Type | Sets the type of memory card for Slot 2. |
| Use Single Card For Playlist | swanstation_MemoryCards_UsePlaylistTitle | When using a playlist (m3u) and per-game (title) memory cards, a single memory card will be used for all discs. If unchecked, a separate card will be used for each disc. |
| Multitap Mode | swanstation_ControllerPorts_MultitapMode | Sets the mode for the multitap. |
| DualShock Analog Mode Combo | swanstation_Controller_AnalogCombo | Sets the combo used to toggle analog mode. |
| DualShock Enable Rumble | swanstation_Controller_EnableRumble | Enable haptic feedback when using a rumble-equipped gamepad with input device set to 'DualShock'. |
| GunCon Show Crosshair | swanstation_Controller_ShowCrosshair | Show a crosshair when the input device is set to 'Namco GunCon'. |
| Controller 1 Force Analog Mode | swanstation_Controller1_ForceAnalog | Forces analog mode to be always on. May cause issues with some games. Only use this option for games that support analog mode but do not automatically enable it themselves. When disabled, analog mode can be toggled by pressing and holding the DualSh |
| Controller 1 Use Analog Sticks for D-Pad in Digital Mode | swanstation_Controller1_AnalogDPadInDigitalMode | Allows you to use the analog sticks to control the d-pad in digital mode, as well as the buttons. |
| Controller 1 Analog Axis Scale | swanstation_Controller1_AxisScale | Sets the analog stick axis scaling factor. |
| Controller 1 Vibration Bias | swanstation_Controller1_VibrationBias | Applies an offset to vibration intensities, higher values will make smaller vibrations more noticable. |
| Controller 1 Lightgun X Scale | swanstation_Controller1_XScale | Scales X coordinates relative to the center of the screen. |
| Controller 1 Lightgun Y Scale | swanstation_Controller1_YScale | Scales Y coordinates relative to the center of the screen. |
| Controller 1 NeGcon Steering Axis Deadzone | swanstation_Controller1_SteeringDeadzone | Sets deadzone size for steering axis. |
| Controller 1 NeGcon Twist Response | swanstation_Controller1_TwistResponse | Sets the twist response type for the left analog stick. 'Quadratic' allows for greater precision than 'Linear' when making small movements, and is more suited for modern controllers, While 'Cubic' further increases small movement precision, but 'exa |
| Controller 2 Force Analog Mode | swanstation_Controller2_ForceAnalog | Forces analog mode to be always on. May cause issues with some games. Only use this option for games that support analog mode but do not automatically enable it themselves. When disabled, analog mode can be toggled by pressing and holding the DualSh |
| Controller 2 Use Analog Sticks for D-Pad in Digital Mode | swanstation_Controller2_AnalogDPadInDigitalMode | Allows you to use the analog sticks to control the d-pad in digital mode, as well as the buttons. |
| Controller 2 Analog Axis Scale | swanstation_Controller2_AxisScale | Sets the analog stick axis scaling factor. |
| Controller 2 Vibration Bias | swanstation_Controller2_VibrationBias | Applies an offset to vibration intensities, higher values will make smaller vibrations more noticable. |
| Controller 2 Lightgun X Scale | swanstation_Controller2_XScale | Scales X coordinates relative to the center of the screen. |
| Controller 2 Lightgun Y Scale | swanstation_Controller2_YScale | Scales Y coordinates relative to the center of the screen. |
| Controller 2 NeGcon Steering Axis Deadzone | swanstation_Controller2_SteeringDeadzone | Sets deadzone size for steering axis. |
| Controller 2 NeGcon Twist Response | swanstation_Controller2_TwistResponse | Sets the twist response type for the left analog stick. 'Quadratic' allows for greater precision than 'Linear' when making small movements, and is more suited for modern controllers, While 'Cubic' further increases small movement precision, but 'exa |
| Controller 3 Force Analog Mode | swanstation_Controller3_ForceAnalog | Forces analog mode to be always on. May cause issues with some games. Only use this option for games that support analog mode but do not automatically enable it themselves. When disabled, analog mode can be toggled by pressing and holding the DualSh |
| Controller 3 Use Analog Sticks for D-Pad in Digital Mode | swanstation_Controller3_AnalogDPadInDigitalMode | Allows you to use the analog sticks to control the d-pad in digital mode, as well as the buttons. |
| Controller 3 Analog Axis Scale | swanstation_Controller3_AxisScale | Sets the analog stick axis scaling factor. |
| Controller 3 Vibration Bias | swanstation_Controller3_VibrationBias | Applies an offset to vibration intensities, higher values will make smaller vibrations more noticable. |
| Controller 3 NeGcon Steering Axis Deadzone | swanstation_Controller3_SteeringDeadzone | Sets deadzone size for steering axis. |
| Controller 3 NeGcon Twist Response | swanstation_Controller3_TwistResponse | Sets the twist response type for the left analog stick. 'Quadratic' allows for greater precision than 'Linear' when making small movements, and is more suited for modern controllers, While 'Cubic' further increases small movement precision, but 'exa |
| Controller 4 Force Analog Mode | swanstation_Controller4_ForceAnalog | Forces analog mode to be always on. May cause issues with some games. Only use this option for games that support analog mode but do not automatically enable it themselves. When disabled, analog mode can be toggled by pressing and holding the DualSh |
| Controller 4 Use Analog Sticks for D-Pad in Digital Mode | swanstation_Controller4_AnalogDPadInDigitalMode | Allows you to use the analog sticks to control the d-pad in digital mode, as well as the buttons. |
| Controller 4 Analog Axis Scale | swanstation_Controller4_AxisScale | Sets the analog stick axis scaling factor. |
| Controller 4 Vibration Bias | swanstation_Controller4_VibrationBias | Applies an offset to vibration intensities, higher values will make smaller vibrations more noticable. |
| Controller 4 NeGcon Steering Axis Deadzone | swanstation_Controller4_SteeringDeadzone | Sets deadzone size for steering axis. |
| Controller 4 NeGcon Twist Response | swanstation_Controller4_TwistResponse | Sets the twist response type for the left analog stick. 'Quadratic' allows for greater precision than 'Linear' when making small movements, and is more suited for modern controllers, While 'Cubic' further increases small movement precision, but 'exa |
| Controller 5 Force Analog Mode | swanstation_Controller5_ForceAnalog | Forces analog mode to be always on. May cause issues with some games. Only use this option for games that support analog mode but do not automatically enable it themselves. When disabled, analog mode can be toggled by pressing and holding the DualSh |
| Controller 5 Use Analog Sticks for D-Pad in Digital Mode | swanstation_Controller5_AnalogDPadInDigitalMode | Allows you to use the analog sticks to control the d-pad in digital mode, as well as the buttons. |
| Controller 5 Analog Axis Scale | swanstation_Controller5_AxisScale | Sets the analog stick axis scaling factor. |
| Controller 5 Vibration Bias | swanstation_Controller5_VibrationBias | Applies an offset to vibration intensities, higher values will make smaller vibrations more noticable. |
| Controller 6 Force Analog Mode | swanstation_Controller6_ForceAnalog | Forces analog mode to be always on. May cause issues with some games. Only use this option for games that support analog mode but do not automatically enable it themselves. When disabled, analog mode can be toggled by pressing and holding the DualSh |
| Controller 6 Use Analog Sticks for D-Pad in Digital Mode | swanstation_Controller6_AnalogDPadInDigitalMode | Allows you to use the analog sticks to control the d-pad in digital mode, as well as the buttons. |
| Controller 6 Analog Axis Scale | swanstation_Controller6_AxisScale | Sets the analog stick axis scaling factor. |
| Controller 6 Vibration Bias | swanstation_Controller6_VibrationBias | Applies an offset to vibration intensities, higher values will make smaller vibrations more noticable. |
| Controller 7 Force Analog Mode | swanstation_Controller7_ForceAnalog | Forces analog mode to be always on. May cause issues with some games. Only use this option for games that support analog mode but do not automatically enable it themselves. When disabled, analog mode can be toggled by pressing and holding the DualSh |
| Controller 7 Use Analog Sticks for D-Pad in Digital Mode | swanstation_Controller7_AnalogDPadInDigitalMode | Allows you to use the analog sticks to control the d-pad in digital mode, as well as the buttons. |
| Controller 7 Analog Axis Scale | swanstation_Controller7_AxisScale | Sets the analog stick axis scaling factor. |
| Controller 7 Vibration Bias | swanstation_Controller7_VibrationBias | Applies an offset to vibration intensities, higher values will make smaller vibrations more noticable. |
| Controller 8 Force Analog Mode | swanstation_Controller8_ForceAnalog | Forces analog mode to be always on. May cause issues with some games. Only use this option for games that support analog mode but do not automatically enable it themselves. When disabled, analog mode can be toggled by pressing and holding the DualSh |
| Controller 8 Use Analog Sticks for D-Pad in Digital Mode | swanstation_Controller8_AnalogDPadInDigitalMode | Allows you to use the analog sticks to control the d-pad in digital mode, as well as the buttons. |
| Controller 8 Analog Axis Scale | swanstation_Controller8_AxisScale | Sets the analog stick axis scaling factor. |
| Controller 8 Vibration Bias | swanstation_Controller8_VibrationBias | Applies an offset to vibration intensities, higher values will make smaller vibrations more noticable. |
| CD-ROM Async Readahead | swanstation_CDROM_ReadaheadSectors | Determines how far the CD-ROM thread will read ahead. Can reduce hitches on slow storage mediums or with compressed games. |
| CPU Overclocking | swanstation_CPU_Overclock | Runs the emulated CPU faster or slower than native speed, which can improve framerates in some games. Will break other games and increase system requirements, use with caution. |
| Apply Compatibility Settings | swanstation_Main_ApplyGameSettings | Automatically disables enhancements on games which are incompatible. |
| Log Level | swanstation_Logging_LogLevel | Sets the level of information logged by the core. |
| CPU Recompiler ICache | swanstation_CPU_RecompilerICache | Determines whether the CPU's instruction cache is simulated in the recompiler. Improves accuracy at a small cost to performance. If games are running too fast, try enabling this option. |
| CPU Recompiler Block Linking | swanstation_CPU_RecompilerBlockLinking | Enables the generated code to directly jump between blocks without going through the dispatcher. Provides a measurable speed boost. |
| CPU Recompiler Fast Memory Access | swanstation_CPU_FastmemMode | Uses page faults to determine hardware memory accesses at runtime. Can provide a significant performance improvement in some games, but make the core more difficult to debug. |
| CPU Recompiler Fast Memory Access Rewrite | swanstation_CPU_FastmemRewrite | Enables rewrites when CPU Recompiler Fast Memory Access is enabled. Can provide a measurable speed boost, but may cause the core to segfault on certain platforms. |
| Enable VRAM Write Texture Replacement | swanstation_TextureReplacements_EnableVRAMWriteReplacements | Replace WRAM write textures with DuckStation formatted texture packs from the textures folder inside the RetroArch install directory. Currently only works with the Vulkan renderer. |
| Preload Texture Replacements | swanstation_TextureReplacements_PreloadTextures | Preload VRAM write replacement textures to RAM |
| Internal Run-Ahead | swanstation_Main_RunaheadFrameCount | Simulates the system ahead of time and rolls back/replays to reduce input lag. Has very high system requirements. |
| Enable 8MB RAM (Dev Console) | swanstation_Console_Enable8MBRAM | Enabled an additional 6MB of RAM, usually present on dev consoles. Games have to use a larger heap size for this additional RAM to be usable, and may break games which rely on memory mirroring, so it should only be used with compatible mods. |
| Use Old MDEC Routines | swanstation_Hacks_UseOldMDECRoutines | Use old routines for MDEC content. |
| Use Alternative Audio Hook (Restart) | swanstation_Audio_FastHook | Use a faster and more efficient to submit audio samples to the frontend. Mostly safe to enable, but may hang for a select few games that rely on the old method to function. Requires the core to be restarted to apply. |
| **Raspberry Pi 3 / Zero 2** {: colspan=3} |
| Region | pcsx_rearmed_region | Specify which region the system is from. 'NTSC' is 60 Hz while 'PAL' is 50 Hz. 'Auto' will detect the region of the currently loaded content. Games may run faster or slower than normal if the incorrect region is selected. |
| BIOS Selection | pcsx_rearmed_bios | Specify which BIOS to use. 'Auto' will attempt to load a real bios file from the frontend 'system' directory, falling back to high level emulation if unavailable. 'HLE' forces high level BIOS emulation. It is recommended to use an official bios file |
| Show BIOS Boot Logo | pcsx_rearmed_show_bios_bootlogo | When using an official BIOS file, specify whether to show the PlayStation logo upon starting or resetting content. Warning: Enabling the boot logo may reduce game compatibility. |
| Enable Second Memory Card (Shared) | pcsx_rearmed_memcard2 | Emulate a second memory card in slot 2. This will be shared by all games. |
| Dynamic Recompiler | pcsx_rearmed_drc | Dynamically recompile PSX CPU instructions to native instructions. Much faster than using an interpreter, but may be less accurate on some platforms. |
| PSX CPU Clock Speed | pcsx_rearmed_psxclock | Overclock or under-clock the PSX CPU. Try adjusting this if the game is too slow, too fast or hangs. Default is 57. |
| (GPU) Slow linked list processing | pcsx_rearmed_gpu_slow_llists | Slower but more accurate GPU linked list processing. Needed by only a few games like Vampire Hunter D. Should be autodetected in most cases. |
| (GPU) Show Interlaced Video | pcsx_rearmed_neon_interlace_enable_v2 | When enabled, games that run in high resolution video modes (480i, 512i) will produced interlaced video output. While this displays correctly on CRT televisions, it will produce artifacts on modern displays. When disabled, all video is output in pro |
| Audio Reverb Effects | pcsx_rearmed_spu_reverb | Enable emulation of the reverb feature provided by the PSX SPU. Can be disabled to improve performance at the expense of reduced audio quality/authenticity. |
| Sound Interpolation | pcsx_rearmed_spu_interpolation | Enable emulation of the in-built audio interpolation provided by the PSX SPU. 'Gaussian' sounds closest to original hardware. 'Simple' improves performance but reduces quality. 'Cubic' has the highest performance requirements but produces increased  |
| CD Audio | pcsx_rearmed_nocdaudio | Enable playback of CD (CD-DA) audio tracks. Can be disabled to improve performance in games that include CD audio, at the expense of missing music. |
| XA Decoding | pcsx_rearmed_noxadecoding | Enable playback of XA (eXtended Architecture ADPCM) audio tracks. Can be disabled to improve performance in games that include XA audio, at the expense of missing music. |
| Threaded SPU | pcsx_rearmed_spu_thread | Emulates the PSX SPU on another CPU thread. May cause audio glitches in some games. |
| Analog Axis Bounds | pcsx_rearmed_analog_axis_modifier | Specify range limits for the left and right analog sticks when input device is set to 'analog' or 'dualshock'. 'Square' bounds improve input response when using controllers with highly circular ranges that are unable to fully saturate the X and Y ax |
| Rumble Effects | pcsx_rearmed_vibration | Enable haptic feedback when using a rumble-equipped gamepad with input device set to 'dualshock'. |
| DualShock Analog Mode Toggle Key Combo | pcsx_rearmed_analog_combo | When the input device type is DualShock, this option allows the emulated DualShock to be toggled between DIGITAL and ANALOG mode like original hardware. You can select the button combination for this. |
| Multitap Mode | pcsx_rearmed_multitap | Connect a virtual PSX Multitap peripheral to either controller 'Port 1' or controller 'Port 2' for 5 player simultaneous input, or to both 'Ports 1 and 2' for 8 player input. Mutlitap usage requires compatible games. |
| NegCon Twist Deadzone | pcsx_rearmed_negcon_deadzone | Set the deadzone of the RetroPad left analog stick when simulating the 'twist' action of emulated neGcon Controllers. Used to eliminate drift/unwanted input. |
| NegCon Twist Response | pcsx_rearmed_negcon_response | Specify the analog response when using a RetroPad left analog stick to simulate the 'twist' action of emulated neGcon Controllers. |
| Mouse Sensitivity | pcsx_rearmed_input_sensitivity | Adjust responsiveness of emulated 'mouse' input devices. |
| Player 1 Lightgun Crosshair | pcsx_rearmed_crosshair1 | Toggle player 1's crosshair for the Guncon or Konami Gun |
| Player 2 Lightgun Crosshair | pcsx_rearmed_crosshair2 | Toggle player 2's crosshair for the Guncon or Konami Gun |
| Konami Gun X Axis Offset | pcsx_rearmed_konamigunadjustx | Apply an X axis offset to light gun input when emulating a Konami Gun (Hyper Blaster / Justifier) device. Can be used to correct aiming misalignments. |
| Konami Gun Y Axis Offset | pcsx_rearmed_konamigunadjusty | Apply a Y axis offset to light gun input when emulating a Konami Gun (Hyper Blaster / Justifier) device. Can be used to correct aiming misalignments. |
| Guncon X Axis Offset | pcsx_rearmed_gunconadjustx | Apply an X axis offset to light gun input when emulating a Guncon device. Can be used to correct aiming misalignments. |
| Guncon Y Axis Offset | pcsx_rearmed_gunconadjusty | Apply a Y axis offset to light gun input when emulating a Guncon device. Can be used to correct aiming misalignments. |
| Guncon X Axis Response | pcsx_rearmed_gunconadjustratiox | Adjust relative magnitude of horizontal light gun motion when emulating a Guncon device. Can be used to correct aiming misalignments. |
| Guncon Y Axis Response | pcsx_rearmed_gunconadjustratioy | Adjust relative magnitude of vertical light gun motion when emulating a Guncon device. Can be used to correct aiming misalignments. |
| Instruction Cache Emulation | pcsx_rearmed_icache_emulation | Enable emulation of the PSX CPU instruction cache. Improves accuracy at the expense of increased performance overheads. Required for Formula One 2001, Formula One Arcade and Formula One 99. [Interpreter only; partial on lightrec and ARM dynarecs] |
| Exception and Breakpoint Emulation | pcsx_rearmed_exception_emulation | Enable emulation of some almost never used PSX's debug features. This causes a performance hit, is not useful for games and is intended for PSX homebrew and romhack developers only. Only enable if you know what you are doing. [Interpreter only] |
| Disable Automatic Compatibility Hacks | pcsx_rearmed_nocompathacks | By default, PCSX-ReARMed will apply auxiliary compatibility hacks automatically, based on the currently loaded content. This behaviour is required for correct operation, but may be disabled if desired. |
| Disable CPU/GTE Stalls | pcsx_rearmed_nostalls | Will cause some games to run too quickly. |
| (Speed Hack) Disable SMC Checks | pcsx_rearmed_nosmccheck | Will cause crashes when loading, and lead to memory card failure. |
| (Speed Hack) Assume GTE Registers Unneeded | pcsx_rearmed_gteregsunneeded | May cause rendering errors. |
| (Speed Hack) Disable GTE Flags | pcsx_rearmed_nogteflags | Will cause rendering errors. |

## Panasonic 3DO

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| BIOS (rom1) | opera_bios | Select which official system BIOS (hardware revision) to use when performing emulation. Only files present in RetroArch's system directory are listed. |
| Font (rom2) | opera_font | Select which official 'font rom' to use when performing emulation. Required by some Japanese games, otherwise optional. Only files present in RetroArch's system directory are listed. |
| CPU Overclock | opera_cpu_overclock | Increase clock speed of the emulated 3DO's 12.5MHz ARM60 CPU. Dramatically improves frame rates in many games (e.g. The Need For Speed), but increases performance requirements and in some cases has no effect (or may cause glitches). |
| Mode | opera_region | Select the resolution and field rate. NOTE: some EU games require a EU ROM. |
| VDLP Bypass CLUT | opera_vdlp_bypass_clut | Force 3DO VDLP to bypass the game's CLUT (color lookup table). May result in incorrect colors but faster rendering. |
| MADAM Matrix Engine | opera_madam_matrix_engine | 'MADAM' is the 3DO's graphics accelerator. It contains a custom maths co-processor, used by the 3DO's CPU to offload matrix operations. This corresponds to running in 'Hardware' - but the 3DO could also utilise a built-in ARM 'Software' version of t |
| OperaOS SWI HLE | opera_swi_hle | 3DO games are built on top of Portfolio OS. Opera has high level emulation of certain OS functions. This HLE may improve performance in on certain games. |
| Threaded DSP | opera_dsp_threaded | Run the DSP (audio processor) on a separate CPU thread. Improves performance on multi-core systems. !EXPERIMENTAL! |
| NVRAM Storage | opera_nvram_storage | Selects whether NVRAM saves should be created per-game or as a single NVRAM file shared between all games. |
| NVRAM Version | opera_nvram_version | Select the NVRAM version. |
| Active Input Devices | opera_active_devices | There exists a bug (perhaps in Opera itself, but possibly in certain games) where having more than 1 emulated controller causes content to ignore gamepad input. Setting 'Active Input Devices' to 1 provides a workaround for this issue. |
| Hide Lightgun Crosshairs | opera_hide_lightgun_crosshairs | Hides lightgun crosshairs for all players. |
| Timing Hack 1 (Crash 'n Burn) | opera_hack_timing_1 | This must be enabled for correct operation of the game 'Crash 'n Burn'. |
| Timing Hack 3 (Dinopark Tycoon) | opera_hack_timing_3 | This must be enabled for correct operation of the game 'Dinopark Tycoon'. |
| Timing Hack 5 (Microcosm) | opera_hack_timing_5 | This must be enabled for correct operation of the game 'Microcosm'. |
| Timing Hack 6 (Alone in the Dark) | opera_hack_timing_6 | This must be enabled for correct operation of the game 'Alone in the Dark'. |
| Graphics Step Y Hack (Samurai Showdown) | opera_hack_graphics_step_y | This must be enabled for backgrounds to render correctly when running the game 'Samurai Showdown'. |
| Debug Output | opera_kprint | Print 3DO debug port output to stderr. Only really useful to 3DO homebrew developers. |

## Philips CD-I

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Read configuration | same_cdi_read_config | n/a |
| Write configuration | same_cdi_write_config | n/a |
| Save state naming | same_cdi_saves | n/a |
| NVRAM Saves per game | same_cdi_nvram_saves | n/a |
| Auto save/load states | same_cdi_auto_save | n/a |
| Enable in-game mouse | same_cdi_mouse_enable | n/a |
| Lightgun mode | same_cdi_lightgun_mode | n/a |
| Profile Buttons according to games (Restart) | same_cdi_buttons_profiles | n/a |
| Enable throttle | same_cdi_throttle | n/a |
| Enable cheats | same_cdi_cheats_enable | n/a |
| Main CPU Overclock | same_cdi_cpu_overclock | n/a |
| MAME Joystick 4-way simulation | same_cdi_mame_4way_enable | n/a |

## Amstrad CPC

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Controls > User 1 Controller Config | cap32_retrojoy0 | n/a |
| Controls > User 2 Controller Config | cap32_retrojoy1 | n/a |
| Controls > Combo Key | cap32_combokey | n/a |
| Controls > Use internal Remap DB | cap32_db_mapkeys | n/a |
| Light Gun > Input | cap32_lightgun_input | n/a |
| Light Gun > Show Crosshair | cap32_lightgun_show | n/a |
| Model | cap32_model | n/a |
| Advanced > Autorun | cap32_autorun | n/a |
| Advanced > Ram size | cap32_ram | n/a |
| Video > Green Phosphor blueish | cap32_advanced_green_phosphor | n/a |
| Video > Monitor Intensity | cap32_scr_intensity | n/a |
| Status Bar | cap32_statusbar | n/a |
| Keyboard Transparency | cap32_keyboard_transparency | n/a |
| Floppy Sound | cap32_floppy_sound | n/a |
| Monitor Type | cap32_scr_tube | n/a |
| CPC Language | cap32_lang_layout | n/a |

## Commodore 64

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| System > Model | vice_c64_model | 'Automatic' switches region per file path tags.</br>Changing while running resets the system! |
| System > RAM Expansion Unit | vice_ram_expansion_unit | Changing while running resets the system! |
| System > Printer | vice_printer | Output is written to 'saves/vice_printer.txt'. |
| System > JiffyDOS | vice_jiffydos | 'True Drive Emulation' & 1541/1571/1581 drive & ROMs required in 'system/vice':</br>- 'JiffyDOS_C64.bin' </br>- 'JiffyDOS_1541-II.bin' </br>- 'JiffyDOS_1571_repl310654.bin' </br>- 'JiffyDOS_1581.bin' |
| System > Read 'vicerc' | vice_read_vicerc | Process first found 'vicerc' in this order:</br>1. 'saves/[content].vicerc'</br>2. 'saves/vicerc'</br>3. 'system/vice/vicerc' |
| System > Reset Type | vice_reset | Reset hotkey action. Core restart will autostart.</br>- 'Autostart' hard resets and reruns content.</br>- 'Soft' keeps some code in memory.</br>- 'Hard' erases all memory.</br>- 'Freeze' is for cartridges. |
| Audio > Drive Sound Emulation | vice_drive_sound_emulation | 'True Drive Emulation' & D64/D71 disk image required. |
| Audio > Datasette Sound | vice_datasette_sound | TAP tape image required. |
| Audio > VIC-II Audio Leak Emulation | vice_audio_leak_emulation | Graphic chip to audio leak emulation. |
| Audio > SID Engine | vice_sid_engine | 'ReSID' is accurate, 'ReSID-FP' is more accurate, 'FastSID' is the last resort. |
| Audio > SID Model | vice_sid_model | C64 has '6581', C64C has '8580'. |
| Audio > SID Extra | vice_sid_extra | Second SID base address. |
| Audio > ReSID Sampling | vice_resid_sampling | 'Resampling' provides best quality. 'Fast' improves performance dramatically on PS Vita. |
| Audio > ReSID Filter Passband | vice_resid_passband | Resampling filter passband in percentage of the total bandwidth. |
| Audio > ReSID Filter Gain | vice_resid_gain | Filter gain in percent. |
| Audio > ReSID Filter 6581 Bias | vice_resid_filterbias | Filter bias for 6581, which can be used to adjust DAC bias in millivolts. |
| Audio > ReSID Filter 8580 Bias | vice_resid_8580filterbias | Filter bias for 8580, which can be used to adjust DAC bias in millivolts. |
| Audio > SFX Sound Expander | vice_sfx_sound_expander | Sound synthesizer cartridge with 9 voices. |
| Audio > Sample Rate | vice_sound_sample_rate | Sound sample rate in Hz. |
| Video > VIC-II Filter | vice_vicii_filter | PAL emulation filter with custom horizontal blur. |
| Video > VIC-II Filter Oddline Offset | vice_vicii_filter_oddline_offset | PAL emulation filter oddline offset. |
| Video > VIC-II Filter Oddline Phase | vice_vicii_filter_oddline_phase | PAL emulation filter oddline phase. Applies with 'Internal' palette only! |
| Video > VIC-II Color Palette | vice_external_palette | 'Colodore' is recommended for most accurate colors. |
| Video > VIC-II Color Gamma | vice_vicii_color_gamma | Gamma for the internal palette. |
| Video > VIC-II Color Brightness | vice_vicii_color_brightness | Brightness for the internal palette. |
| Video > VIC-II Color Contrast | vice_vicii_color_contrast | Contrast for the internal palette. |
| Video > VIC-II Color Saturation | vice_vicii_color_saturation | Saturation for the internal palette. |
| Video > VIC-II Color Tint | vice_vicii_color_tint | Tint for the internal palette. |
| Video > Color Depth | vice_gfx_colors | Full restart required. |
| Media > Automatic Load Warp | vice_autoloadwarp | Toggle warp mode during disk and/or tape access if there is no audio output. Mutes 'Drive Sound Emulation', 'Datasette Sound' and 'Audio Leak Emulation' when not ignoring audio.</br>'True Drive Emulation' required with disks! |
| Media > Warp Boost | vice_warp_boost | Make warp mode much faster by changing SID emulation to 'FastSID' while warping. |
| Media > Autostart | vice_autostart | 'ON' always runs content, 'OFF' runs only PRG/CRT, 'Warp' turns warp mode on during autostart loading. |
| Media > True Drive Emulation | vice_drive_true_emulation | Loads much slower, but some games need it.</br>Required for 'JiffyDOS', 'Automatic Load Warp' and LED driver interface! |
| Media > Virtual Device Traps | vice_virtual_device_traps | Required for printer device, but causes loading issues on rare cases. |
| Media > Floppy Write Protection | vice_floppy_write_protection | Set device 8 read only. |
| Media > EasyFlash Write Protection | vice_easyflash_write_protection | Set EasyFlash cartridges read only. |
| Media > Global Work Disk | vice_work_disk | Work disk in device 8 will not be inserted when floppy content is launched. Files and directories are named 'vice_work'. |
| Media > Cartridge | vice_cartridge | Cartridge images go in 'system/vice/C64'.</br>Changing while running resets the system! |
| Input > Analog Stick Mouse | vice_analogmouse | Override analog stick remappings when non-joysticks are used. 'OFF' controls mouse/paddles with both analogs when remappings are empty. |
| Input > Analog Stick Mouse Deadzone | vice_analogmouse_deadzone | Required distance from stick center to register input. |
| Input > Analog Stick Mouse Speed | vice_analogmouse_speed | Mouse movement speed multiplier for analog stick. |
| Input > D-Pad Mouse Speed | vice_dpadmouse_speed | Mouse movement speed multiplier for directional pad. |
| Input > Mouse Speed | vice_mouse_speed | Global mouse speed. |
| Input > Keyboard Pass-through | vice_physical_keyboard_pass_through | 'ON' passes all physical keyboard events to the core. 'OFF' prevents RetroPad keys from generating keyboard events. |
| Input > Datasette Hotkeys | vice_datasette_hotkeys | Toggle all Datasette hotkeys. |
| Input > Keyrah Keypad Mappings | vice_keyrah_keypad_mappings | Hardcoded keypad to joyport mappings for Keyrah hardware. |
| Input > Keyboard Keymap | vice_keyboard_keymap | User-defined keymaps go in 'system/vice/C64'.</br>- Positional: 'sdl_pos.vkm'</br>- Symbolic: 'sdl_sym.vkm' |
| RetroPad > Turbo Fire | vice_turbo_fire | Hotkey toggling disables this option until core restart. |
| RetroPad > Turbo Button | vice_turbo_fire_button | Replace the mapped button with turbo fire button. |
| RetroPad > Turbo Pulse | vice_turbo_pulse | Frames in a button cycle.</br>- '2' = 1 frame down, 1 frame up</br>- '4' = 2 frames down, 2 frames up</br>- '6' = 3 frames down, 3 frames up</br>etc. |
| Input > Userport Joystick Adapter | vice_userport_joytype | Required for more than 2 joysticks, for example IK+ Gold with 3 players. |
| RetroPad > Joystick Port | vice_joyport | Most games use port 2, some use port 1.</br>Filename forcing or hotkey toggling disables this option until core restart. |
| RetroPad > Joystick Port Type | vice_joyport_type | Non-joysticks are plugged in current port only and are controlled with left analog stick or mouse. Paddles are split to 1st and 2nd RetroPort. |
| RetroPad > Face Button Options | vice_retropad_options | Rotate face buttons clockwise and/or make 2nd fire press up. |
| Hotkey > Toggle Virtual Keyboard | vice_mapper_vkbd | Press the mapped key to toggle the virtual keyboard. |
| Hotkey > Toggle Statusbar | vice_mapper_statusbar | Press the mapped key to toggle the statusbar. |
| Hotkey > Switch Joyport | vice_mapper_joyport_switch | Press the mapped key to switch joyports 1 & 2.</br>Switching disables 'RetroPad Port' option until core restart. |
| Hotkey > Toggle Turbo Fire | vice_mapper_turbo_fire_toggle | Press the mapped key to toggle turbo fire. |
| Hotkey > Toggle Save Disk | vice_mapper_save_disk_toggle | Press the mapped key to create/insert/eject a save disk. |
| Hotkey > Toggle Aspect Ratio | vice_mapper_aspect_ratio_toggle | Press the mapped key to toggle aspect ratio.</br>Toggling disables 'Pixel Aspect Ratio' option until core restart. |
| Hotkey > Toggle Zoom Mode | vice_mapper_zoom_mode_toggle | Hidden placeholder for backwards compatibility. |
| Hotkey > Toggle Datasette Hotkeys | vice_mapper_datasette_toggle_hotkeys | Press the mapped key to toggle Datasette hotkeys. |
| Hotkey > Datasette PLAY | vice_mapper_datasette_start | Press play on tape. |
| Hotkey > Datasette STOP | vice_mapper_datasette_stop | Press stop on tape. |
| Hotkey > Datasette REWIND | vice_mapper_datasette_rewind | Press rewind on tape. |
| Hotkey > Datasette F.FWD | vice_mapper_datasette_forward | Press fast forward on tape. |
| Hotkey > Datasette RESET | vice_mapper_datasette_reset | Reset tape to beginning. |
| Hotkey > Reset | vice_mapper_reset | Press the mapped key to trigger the selected 'Reset Type'. |
| Hotkey > Hold Warp Mode | vice_mapper_warp_mode | Hold the mapped key for warp mode. |
| RetroPad > Up | vice_mapper_up | Unmapped defaults to joystick up. |
| RetroPad > Down | vice_mapper_down | Unmapped defaults to joystick down. |
| RetroPad > Left | vice_mapper_left | Unmapped defaults to joystick left. |
| RetroPad > Right | vice_mapper_right | Unmapped defaults to joystick right. |
| RetroPad > B | vice_mapper_b | Unmapped defaults to fire button.</br>VKBD: Press selected key. |
| RetroPad > A | vice_mapper_a | Unmapped defaults to 2nd fire button.</br>VKBD: Toggle transparency. Remapping to non-keyboard keys overrides VKBD function! |
| RetroPad > Y | vice_mapper_y | VKBD: Toggle 'ShiftLock'. Remapping to non-keyboard keys overrides VKBD function! |
| RetroPad > X | vice_mapper_x | VKBD: Press 'Space'. Remapping to non-keyboard keys overrides VKBD function! |
| RetroPad > Select | vice_mapper_select | VKBD comes up with RetroPad Select by default. |
| RetroPad > Start | vice_mapper_start | VKBD: Press 'Return'. Remapping to non-keyboard keys overrides VKBD function! |
| RetroPad > L | vice_mapper_l | n/a |
| RetroPad > R | vice_mapper_r | n/a |
| RetroPad > L2 | vice_mapper_l2 | n/a |
| RetroPad > R2 | vice_mapper_r2 | n/a |
| RetroPad > L3 | vice_mapper_l3 | n/a |
| RetroPad > R3 | vice_mapper_r3 | n/a |
| RetroPad > Left Analog > Up | vice_mapper_lu | n/a |
| RetroPad > Left Analog > Down | vice_mapper_ld | n/a |
| RetroPad > Left Analog > Left | vice_mapper_ll | n/a |
| RetroPad > Left Analog > Right | vice_mapper_lr | n/a |
| RetroPad > Right Analog > Up | vice_mapper_ru | n/a |
| RetroPad > Right Analog > Down | vice_mapper_rd | n/a |
| RetroPad > Right Analog > Left | vice_mapper_rl | n/a |
| RetroPad > Right Analog > Right | vice_mapper_rr | n/a |
| OSD > Virtual KBD Theme | vice_vkbd_theme | The keyboard comes up with RetroPad Select by default. |
| OSD > Virtual KBD Transparency | vice_vkbd_transparency | Keyboard transparency can be toggled with RetroPad A. |
| OSD > Virtual KBD Dimming | vice_vkbd_dimming | Dimming level of the surrounding area. |
| OSD > Statusbar Mode | vice_statusbar | - 'Full': Joyports + Messages + LEDs</br>- 'Basic': Messages + LEDs</br>- 'Minimal': LED colors only |
| OSD > Statusbar Startup | vice_statusbar_startup | Show statusbar on startup. |
| OSD > Statusbar Messages | vice_statusbar_messages | Show messages when statusbar is hidden. |
| OSD > Light Pen/Gun Pointer Color | vice_joyport_pointer_color | Crosshair color for light pens and guns. |

## Commodore Amiga

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| System > Model | puae_model | 'Automatic' defaults to 'A500' with floppy disks, 'A1200' with hard drives and 'CD32' with compact discs. 'Automatic' can be overridden with file path tags.</br></br></br></br>Core restart required. |
| System > Show Automatic Model Options | puae_model_options_display | Show/hide default model options (Floppy/HD/CD) for 'Automatic' model. |
| Model > Automatic Floppy | puae_model_fd | Default model when floppies are launched with 'Automatic' model.</br></br>Core restart required. |
| Model > Automatic HD | puae_model_hd | Default model when HD interface is used with 'Automatic' model. Affects WHDLoad installs and other hard drive images.</br></br>Core restart required. |
| Model > Automatic CD | puae_model_cd | Default model when compact discs are launched with 'Automatic' model.</br></br>Core restart required. |
| System > Kickstart ROM | puae_kickstart | 'Automatic' defaults to the most compatible version for the model. 'AROS' is a built-in replacement with fair compatibility.</br></br>Core restart required. |
| System > Chip RAM | puae_chipmem_size | 'Automatic' defaults to the current preset model.</br></br>Core restart required. |
| System > Slow RAM | puae_bogomem_size | 'Automatic' defaults to the current preset model.</br></br>Core restart required. |
| System > Z2 Fast RAM | puae_fastmem_size | 'Automatic' defaults to the current preset model.</br></br>Core restart required. |
| System > Z3 Fast RAM | puae_z3mem_size | 'Automatic' defaults to the current preset model.</br></br>Core restart required. |
| System > CPU Model | puae_cpu_model | 'Automatic' defaults to the current preset model.</br></br>Core restart required. |
| System > FPU Model | puae_fpu_model | 'Automatic' defaults to the current preset model.</br></br>Core restart required. |
| System > CPU Speed | puae_cpu_throttle | Ignored with 'Cycle-exact'. |
| System > CPU Cycle-exact Speed | puae_cpu_multiplier | Applies only with 'Cycle-exact'. |
| System > CPU Compatibility | puae_cpu_compatibility | Some games have graphic and/or speed issues without 'Cycle-exact'. 'Cycle-exact' can be forced with '(CE)' file path tag. |
| Audio > Stereo Separation | puae_sound_stereo_separation | Paula sound chip channel panning. Does not affect CD audio. |
| Audio > Interpolation | puae_sound_interpol | Paula sound chip interpolation type. |
| Audio > Filter | puae_sound_filter | 'Emulated' allows states between ON/OFF. |
| Audio > Filter Type | puae_sound_filter_type | 'Automatic' picks the filter type for the hardware. |
| Audio > Floppy Sound Emulation | puae_floppy_sound | Floppy volume in percent. |
| Audio > Floppy Sound Mute Ejected | puae_floppy_sound_empty_mute | Mute drive head clicking when floppy is not inserted. |
| Audio > Floppy Sound Type | puae_floppy_sound_type | External files go in 'system/uae/' or 'system/uae_data/'. |
| Audio > CD Audio Volume | puae_sound_volume_cd | CD volume in percent. |
| Video > Allow Hz Change | puae_video_allow_hz_change | Let Amiga decide the exact refresh rate when interlace mode or PAL/NTSC changes. 'Locked' changes only when video standard changes.</br></br>Core restart required. |
| Video > Standard | puae_video_standard | Output Hz & height:</br>- 'PAL': 50Hz - 288px / 576px</br>- 'NTSC': 60Hz - 240px / 480px</br>- 'Automatic' switches region per file path tags. |
| Video > Immediate/Waiting Blits | puae_immediate_blits | - 'Immediate Blitter': Faster but less compatible blitter emulation.</br>- 'Wait for Blitter': Compatibility hack for programs that don't wait for the blitter correctly. |
| Video > Collision Level | puae_collision_level | 'Sprites and Playfields' is recommended. |
| Video > Color Gamma | puae_gfx_gamma | Adjust color gamma. |
| Media > Automatic Load Fast-Forward | puae_autoloadfastforward | Toggle frontend fast-forward during media access if there is no audio output. Mutes 'Floppy Sound Emulation'. |
| Media > Floppy Speed | puae_floppy_speed | Default speed is 300RPM. 'Turbo' removes disk rotation emulation. |
| Media > Floppy MultiDrive | puae_floppy_multidrive | Insert each disk in different drives. Can be forced with '(MD)' file path tag. Maximum is 4 disks due to external drive limit! Not all games support external drives!</br></br>Core restart required. |
| Media > Floppy Write Protection | puae_floppy_write_protection | Set all drives read only. Changing this while emulation is running ejects and reinserts all disks. IPF images are always read-only! |
| Media > Floppy Write Redirect | puae_floppy_write_redirect | Writes to a substitute disk under 'saves' instead of original disks. Works also with IPF images. |
| Media > CD Speed | puae_cd_speed | Transfer rate in CD32 is 300KB/s (double-speed), CDTV is 150KB/s (single-speed). 'Turbo' removes seek delay emulation. |
| Media > CD Startup Delayed Insert | puae_cd_startup_delayed_insert | Some games fail to load if CD32/CDTV is powered on with CD inserted. 'ON' inserts CD during boot animation. |
| Media > CD32/CDTV Shared NVRAM | puae_shared_nvram | 'OFF' saves separate files per content. Starting without content uses the shared file. CD32 and CDTV use separate shared files.</br></br>Core restart required. |
| Media > WHDLoad Support | puae_use_whdload | Enable launching pre-installed WHDLoad installs. Creates a helper boot image for loading content and an empty image for saving. Legacy 'HDFs' mode is not recommended!</br></br>Core restart required.</br>- 'Files' creates data in directories</br>- 'HDFs' creates data |
| Media > WHDLoad Theme | puae_use_whdload_theme | AmigaOS 'system-configuration' color prefs in WHDLoad helper image. Available only with 'Files' mode.</br></br>Core restart required.</br>- 'Default' = Black/White/DarkGray/LightGray</br>- 'Native' = Gray/Black/White/LightBlue |
| Media > WHDLoad Splash Screen | puae_use_whdload_prefs | Space/Enter/Fire works as WHDLoad Start-button. </br></br>Core restart required.</br></br>Override with buttons while booting:</br>- 'Config': Hold 2nd fire / Blue</br>- 'Splash': Hold LMB</br>- 'Config + Splash': Hold RMB</br>- ReadMe + MkCustom: Hold Red+Blue |
| Media > WHDLoad NoWriteCache | puae_use_whdload_nowritecache | Write save data immediately or on WHDLoad quit. Write cache enabled runs the core a few frames after frontend quit in order to trigger WHDLoad quit and flush the cache.</br></br>Core restart required. |
| Media > Global Boot HD | puae_use_boot_hd | Attach a hard disk meant for Workbench, not for WHDLoad! Enabling forces a model with HD interface. Changing HDF size will not replace or edit the existing HDF.</br></br>Core restart required. |
| Media > Cartridge | puae_cart_file | Cartridge images go in 'system/uae/' or 'system/uae_data/'.</br></br>Core restart required. |
| Input > Analog Stick Mouse | puae_analogmouse | Default mouse control stick when remappings are empty. |
| Input > Analog Stick Mouse Deadzone | puae_analogmouse_deadzone | Required distance from stick center to register input. |
| Input > Analog Stick Mouse Speed | puae_analogmouse_speed | Mouse movement speed multiplier for analog stick. |
| Input > D-Pad Mouse Speed | puae_dpadmouse_speed | Mouse movement speed multiplier for directional pad. |
| Input > Mouse Speed | puae_mouse_speed | Global mouse speed. |
| Input > Physical Mouse | puae_physicalmouse | 'Double' requirements: raw/udev input driver and proper mouse index per port.</br></br>Does not affect RetroPad emulated mice. |
| Input > Keyboard Pass-through | puae_physical_keyboard_pass_through | 'ON' passes all physical keyboard events to the core. 'OFF' prevents RetroPad keys from generating keyboard events. |
| Input > Keyrah Keypad Mappings | puae_keyrah_keypad_mappings | Hardcoded keypad to joyport mappings for Keyrah hardware. |
| RetroPad > Turbo Fire | puae_turbo_fire | Hotkey toggling disables this option until core restart. |
| RetroPad > Turbo Button | puae_turbo_fire_button | Replace the mapped button with turbo fire button. |
| RetroPad > Turbo Pulse | puae_turbo_pulse | Frames in a button cycle.</br>- '2' = 1 frame down, 1 frame up</br>- '4' = 2 frames down, 2 frames up</br>- '6' = 3 frames down, 3 frames up</br>etc. |
| RetroPad > Joystick/Mouse | puae_joyport | Change D-Pad control between joyports. Hotkey toggling disables this option until core restart. |
| RetroPad > Joystick Port Order | puae_joyport_order | Plug RetroPads in different ports. Useful for 4-player adapters. |
| RetroPad > Face Button Options | puae_retropad_options | Rotate face buttons clockwise and/or make 2nd fire press up. |
| CD32 Pad > Face Button Options | puae_cd32pad_options | Rotate face buttons clockwise and/or make blue button press up. |
| Hotkey > Toggle Virtual Keyboard | puae_mapper_vkbd | Press the mapped key to toggle the virtual keyboard. |
| Hotkey > Toggle Statusbar | puae_mapper_statusbar | Press the mapped key to toggle the statusbar. |
| Hotkey > Switch Joystick/Mouse | puae_mapper_mouse_toggle | Press the mapped key to switch between joystick and mouse control. |
| Hotkey > Toggle Turbo Fire | puae_mapper_turbo_fire_toggle | Press the mapped key to toggle turbo fire. |
| Hotkey > Toggle Save Disk | puae_mapper_save_disk_toggle | Press the mapped key to create/insert/eject a save disk. |
| Hotkey > Toggle Aspect Ratio | puae_mapper_aspect_ratio_toggle | Press the mapped key to toggle between PAL/NTSC pixel aspect ratio. |
| Hotkey > Toggle Zoom Mode | puae_mapper_zoom_mode_toggle | Hidden placeholder for backwards compatibility. |
| Hotkey > Reset | puae_mapper_reset | Press the mapped key to trigger soft reset (Ctrl-Amiga-Amiga). |
| RetroPad > Up | puae_mapper_up | Unmapped defaults to joystick up. |
| RetroPad > Down | puae_mapper_down | Unmapped defaults to joystick down. |
| RetroPad > Left | puae_mapper_left | Unmapped defaults to joystick left. |
| RetroPad > Right | puae_mapper_right | Unmapped defaults to joystick right. |
| RetroPad > B | puae_mapper_b | Unmapped defaults to fire button.</br></br>VKBD: Press selected key. |
| RetroPad > A | puae_mapper_a | Unmapped defaults to 2nd fire button.</br></br>VKBD: Toggle transparency. Remapping to non-keyboard keys overrides VKBD function! |
| RetroPad > Y | puae_mapper_y | VKBD: Toggle 'CapsLock'. Remapping to non-keyboard keys overrides VKBD function! |
| RetroPad > X | puae_mapper_x | VKBD: Press 'Space'. Remapping to non-keyboard keys overrides VKBD function! |
| RetroPad > Select | puae_mapper_select | VKBD comes up with RetroPad Select by default. |
| RetroPad > Start | puae_mapper_start | VKBD: Press 'Return'. Remapping to non-keyboard keys overrides VKBD function! |
| RetroPad > L | puae_mapper_l | n/a |
| RetroPad > R | puae_mapper_r | n/a |
| RetroPad > L2 | puae_mapper_l2 | n/a |
| RetroPad > R2 | puae_mapper_r2 | n/a |
| RetroPad > L3 | puae_mapper_l3 | n/a |
| RetroPad > R3 | puae_mapper_r3 | n/a |
| RetroPad > Left Analog > Up | puae_mapper_lu | n/a |
| RetroPad > Left Analog > Down | puae_mapper_ld | n/a |
| RetroPad > Left Analog > Left | puae_mapper_ll | n/a |
| RetroPad > Left Analog > Right | puae_mapper_lr | n/a |
| RetroPad > Right Analog > Up | puae_mapper_ru | n/a |
| RetroPad > Right Analog > Down | puae_mapper_rd | n/a |
| RetroPad > Right Analog > Left | puae_mapper_rl | n/a |
| RetroPad > Right Analog > Right | puae_mapper_rr | n/a |
| OSD > Virtual KBD Theme | puae_vkbd_theme | The keyboard comes up with RetroPad Select by default. |
| OSD > Virtual KBD Transparency | puae_vkbd_transparency | Keyboard transparency can be toggled with RetroPad A. |
| OSD > Virtual KBD Dimming | puae_vkbd_dimming | Dimming level of the surrounding area. |
| OSD > Statusbar Mode | puae_statusbar | - 'Full': Joyports + Messages + LEDs</br>- 'Basic': Messages + LEDs</br>- 'Minimal': LED colors only |
| OSD > Statusbar Startup | puae_statusbar_startup | Show statusbar on startup. |
| OSD > Statusbar Messages | puae_statusbar_messages | Show messages when statusbar is hidden. |
| OSD > Light Pen/Gun Pointer Color | puae_joyport_pointer_color | Crosshair color for light pens and guns. |

## Commodore Amiga CD32

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| System > Model | puae_model | 'Automatic' defaults to 'A500' with floppy disks, 'A1200' with hard drives and 'CD32' with compact discs. 'Automatic' can be overridden with file path tags.</br></br></br></br>Core restart required. |
| System > Show Automatic Model Options | puae_model_options_display | Show/hide default model options (Floppy/HD/CD) for 'Automatic' model. |
| Model > Automatic Floppy | puae_model_fd | Default model when floppies are launched with 'Automatic' model.</br></br>Core restart required. |
| Model > Automatic HD | puae_model_hd | Default model when HD interface is used with 'Automatic' model. Affects WHDLoad installs and other hard drive images.</br></br>Core restart required. |
| Model > Automatic CD | puae_model_cd | Default model when compact discs are launched with 'Automatic' model.</br></br>Core restart required. |
| System > Kickstart ROM | puae_kickstart | 'Automatic' defaults to the most compatible version for the model. 'AROS' is a built-in replacement with fair compatibility.</br></br>Core restart required. |
| System > Chip RAM | puae_chipmem_size | 'Automatic' defaults to the current preset model.</br></br>Core restart required. |
| System > Slow RAM | puae_bogomem_size | 'Automatic' defaults to the current preset model.</br></br>Core restart required. |
| System > Z2 Fast RAM | puae_fastmem_size | 'Automatic' defaults to the current preset model.</br></br>Core restart required. |
| System > Z3 Fast RAM | puae_z3mem_size | 'Automatic' defaults to the current preset model.</br></br>Core restart required. |
| System > CPU Model | puae_cpu_model | 'Automatic' defaults to the current preset model.</br></br>Core restart required. |
| System > FPU Model | puae_fpu_model | 'Automatic' defaults to the current preset model.</br></br>Core restart required. |
| System > CPU Speed | puae_cpu_throttle | Ignored with 'Cycle-exact'. |
| System > CPU Cycle-exact Speed | puae_cpu_multiplier | Applies only with 'Cycle-exact'. |
| System > CPU Compatibility | puae_cpu_compatibility | Some games have graphic and/or speed issues without 'Cycle-exact'. 'Cycle-exact' can be forced with '(CE)' file path tag. |
| Audio > Stereo Separation | puae_sound_stereo_separation | Paula sound chip channel panning. Does not affect CD audio. |
| Audio > Interpolation | puae_sound_interpol | Paula sound chip interpolation type. |
| Audio > Filter | puae_sound_filter | 'Emulated' allows states between ON/OFF. |
| Audio > Filter Type | puae_sound_filter_type | 'Automatic' picks the filter type for the hardware. |
| Audio > Floppy Sound Emulation | puae_floppy_sound | Floppy volume in percent. |
| Audio > Floppy Sound Mute Ejected | puae_floppy_sound_empty_mute | Mute drive head clicking when floppy is not inserted. |
| Audio > Floppy Sound Type | puae_floppy_sound_type | External files go in 'system/uae/' or 'system/uae_data/'. |
| Audio > CD Audio Volume | puae_sound_volume_cd | CD volume in percent. |
| Video > Allow Hz Change | puae_video_allow_hz_change | Let Amiga decide the exact refresh rate when interlace mode or PAL/NTSC changes. 'Locked' changes only when video standard changes.</br></br>Core restart required. |
| Video > Standard | puae_video_standard | Output Hz & height:</br>- 'PAL': 50Hz - 288px / 576px</br>- 'NTSC': 60Hz - 240px / 480px</br>- 'Automatic' switches region per file path tags. |
| Video > Immediate/Waiting Blits | puae_immediate_blits | - 'Immediate Blitter': Faster but less compatible blitter emulation.</br>- 'Wait for Blitter': Compatibility hack for programs that don't wait for the blitter correctly. |
| Video > Collision Level | puae_collision_level | 'Sprites and Playfields' is recommended. |
| Video > Color Gamma | puae_gfx_gamma | Adjust color gamma. |
| Media > Automatic Load Fast-Forward | puae_autoloadfastforward | Toggle frontend fast-forward during media access if there is no audio output. Mutes 'Floppy Sound Emulation'. |
| Media > Floppy Speed | puae_floppy_speed | Default speed is 300RPM. 'Turbo' removes disk rotation emulation. |
| Media > Floppy MultiDrive | puae_floppy_multidrive | Insert each disk in different drives. Can be forced with '(MD)' file path tag. Maximum is 4 disks due to external drive limit! Not all games support external drives!</br></br>Core restart required. |
| Media > Floppy Write Protection | puae_floppy_write_protection | Set all drives read only. Changing this while emulation is running ejects and reinserts all disks. IPF images are always read-only! |
| Media > Floppy Write Redirect | puae_floppy_write_redirect | Writes to a substitute disk under 'saves' instead of original disks. Works also with IPF images. |
| Media > CD Speed | puae_cd_speed | Transfer rate in CD32 is 300KB/s (double-speed), CDTV is 150KB/s (single-speed). 'Turbo' removes seek delay emulation. |
| Media > CD Startup Delayed Insert | puae_cd_startup_delayed_insert | Some games fail to load if CD32/CDTV is powered on with CD inserted. 'ON' inserts CD during boot animation. |
| Media > CD32/CDTV Shared NVRAM | puae_shared_nvram | 'OFF' saves separate files per content. Starting without content uses the shared file. CD32 and CDTV use separate shared files.</br></br>Core restart required. |
| Media > WHDLoad Support | puae_use_whdload | Enable launching pre-installed WHDLoad installs. Creates a helper boot image for loading content and an empty image for saving. Legacy 'HDFs' mode is not recommended!</br></br>Core restart required.</br>- 'Files' creates data in directories</br>- 'HDFs' creates data |
| Media > WHDLoad Theme | puae_use_whdload_theme | AmigaOS 'system-configuration' color prefs in WHDLoad helper image. Available only with 'Files' mode.</br></br>Core restart required.</br>- 'Default' = Black/White/DarkGray/LightGray</br>- 'Native' = Gray/Black/White/LightBlue |
| Media > WHDLoad Splash Screen | puae_use_whdload_prefs | Space/Enter/Fire works as WHDLoad Start-button. </br></br>Core restart required.</br></br>Override with buttons while booting:</br>- 'Config': Hold 2nd fire / Blue</br>- 'Splash': Hold LMB</br>- 'Config + Splash': Hold RMB</br>- ReadMe + MkCustom: Hold Red+Blue |
| Media > WHDLoad NoWriteCache | puae_use_whdload_nowritecache | Write save data immediately or on WHDLoad quit. Write cache enabled runs the core a few frames after frontend quit in order to trigger WHDLoad quit and flush the cache.</br></br>Core restart required. |
| Media > Global Boot HD | puae_use_boot_hd | Attach a hard disk meant for Workbench, not for WHDLoad! Enabling forces a model with HD interface. Changing HDF size will not replace or edit the existing HDF.</br></br>Core restart required. |
| Media > Cartridge | puae_cart_file | Cartridge images go in 'system/uae/' or 'system/uae_data/'.</br></br>Core restart required. |
| Input > Analog Stick Mouse | puae_analogmouse | Default mouse control stick when remappings are empty. |
| Input > Analog Stick Mouse Deadzone | puae_analogmouse_deadzone | Required distance from stick center to register input. |
| Input > Analog Stick Mouse Speed | puae_analogmouse_speed | Mouse movement speed multiplier for analog stick. |
| Input > D-Pad Mouse Speed | puae_dpadmouse_speed | Mouse movement speed multiplier for directional pad. |
| Input > Mouse Speed | puae_mouse_speed | Global mouse speed. |
| Input > Physical Mouse | puae_physicalmouse | 'Double' requirements: raw/udev input driver and proper mouse index per port.</br></br>Does not affect RetroPad emulated mice. |
| Input > Keyboard Pass-through | puae_physical_keyboard_pass_through | 'ON' passes all physical keyboard events to the core. 'OFF' prevents RetroPad keys from generating keyboard events. |
| Input > Keyrah Keypad Mappings | puae_keyrah_keypad_mappings | Hardcoded keypad to joyport mappings for Keyrah hardware. |
| RetroPad > Turbo Fire | puae_turbo_fire | Hotkey toggling disables this option until core restart. |
| RetroPad > Turbo Button | puae_turbo_fire_button | Replace the mapped button with turbo fire button. |
| RetroPad > Turbo Pulse | puae_turbo_pulse | Frames in a button cycle.</br>- '2' = 1 frame down, 1 frame up</br>- '4' = 2 frames down, 2 frames up</br>- '6' = 3 frames down, 3 frames up</br>etc. |
| RetroPad > Joystick/Mouse | puae_joyport | Change D-Pad control between joyports. Hotkey toggling disables this option until core restart. |
| RetroPad > Joystick Port Order | puae_joyport_order | Plug RetroPads in different ports. Useful for 4-player adapters. |
| RetroPad > Face Button Options | puae_retropad_options | Rotate face buttons clockwise and/or make 2nd fire press up. |
| CD32 Pad > Face Button Options | puae_cd32pad_options | Rotate face buttons clockwise and/or make blue button press up. |
| Hotkey > Toggle Virtual Keyboard | puae_mapper_vkbd | Press the mapped key to toggle the virtual keyboard. |
| Hotkey > Toggle Statusbar | puae_mapper_statusbar | Press the mapped key to toggle the statusbar. |
| Hotkey > Switch Joystick/Mouse | puae_mapper_mouse_toggle | Press the mapped key to switch between joystick and mouse control. |
| Hotkey > Toggle Turbo Fire | puae_mapper_turbo_fire_toggle | Press the mapped key to toggle turbo fire. |
| Hotkey > Toggle Save Disk | puae_mapper_save_disk_toggle | Press the mapped key to create/insert/eject a save disk. |
| Hotkey > Toggle Aspect Ratio | puae_mapper_aspect_ratio_toggle | Press the mapped key to toggle between PAL/NTSC pixel aspect ratio. |
| Hotkey > Toggle Zoom Mode | puae_mapper_zoom_mode_toggle | Hidden placeholder for backwards compatibility. |
| Hotkey > Reset | puae_mapper_reset | Press the mapped key to trigger soft reset (Ctrl-Amiga-Amiga). |
| RetroPad > Up | puae_mapper_up | Unmapped defaults to joystick up. |
| RetroPad > Down | puae_mapper_down | Unmapped defaults to joystick down. |
| RetroPad > Left | puae_mapper_left | Unmapped defaults to joystick left. |
| RetroPad > Right | puae_mapper_right | Unmapped defaults to joystick right. |
| RetroPad > B | puae_mapper_b | Unmapped defaults to fire button.</br></br>VKBD: Press selected key. |
| RetroPad > A | puae_mapper_a | Unmapped defaults to 2nd fire button.</br></br>VKBD: Toggle transparency. Remapping to non-keyboard keys overrides VKBD function! |
| RetroPad > Y | puae_mapper_y | VKBD: Toggle 'CapsLock'. Remapping to non-keyboard keys overrides VKBD function! |
| RetroPad > X | puae_mapper_x | VKBD: Press 'Space'. Remapping to non-keyboard keys overrides VKBD function! |
| RetroPad > Select | puae_mapper_select | VKBD comes up with RetroPad Select by default. |
| RetroPad > Start | puae_mapper_start | VKBD: Press 'Return'. Remapping to non-keyboard keys overrides VKBD function! |
| RetroPad > L | puae_mapper_l | n/a |
| RetroPad > R | puae_mapper_r | n/a |
| RetroPad > L2 | puae_mapper_l2 | n/a |
| RetroPad > R2 | puae_mapper_r2 | n/a |
| RetroPad > L3 | puae_mapper_l3 | n/a |
| RetroPad > R3 | puae_mapper_r3 | n/a |
| RetroPad > Left Analog > Up | puae_mapper_lu | n/a |
| RetroPad > Left Analog > Down | puae_mapper_ld | n/a |
| RetroPad > Left Analog > Left | puae_mapper_ll | n/a |
| RetroPad > Left Analog > Right | puae_mapper_lr | n/a |
| RetroPad > Right Analog > Up | puae_mapper_ru | n/a |
| RetroPad > Right Analog > Down | puae_mapper_rd | n/a |
| RetroPad > Right Analog > Left | puae_mapper_rl | n/a |
| RetroPad > Right Analog > Right | puae_mapper_rr | n/a |
| OSD > Virtual KBD Theme | puae_vkbd_theme | The keyboard comes up with RetroPad Select by default. |
| OSD > Virtual KBD Transparency | puae_vkbd_transparency | Keyboard transparency can be toggled with RetroPad A. |
| OSD > Virtual KBD Dimming | puae_vkbd_dimming | Dimming level of the surrounding area. |
| OSD > Statusbar Mode | puae_statusbar | - 'Full': Joyports + Messages + LEDs</br>- 'Basic': Messages + LEDs</br>- 'Minimal': LED colors only |
| OSD > Statusbar Startup | puae_statusbar_startup | Show statusbar on startup. |
| OSD > Statusbar Messages | puae_statusbar_messages | Show messages when statusbar is hidden. |
| OSD > Light Pen/Gun Pointer Color | puae_joyport_pointer_color | Crosshair color for light pens and guns. |

## Atari ST

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Polarized Audio Filter | hatari_polarized_filter | Uses hatari's polarized lowpass filters on audio to simulate distortion. |
| Autoload hatari.cfg. | hatari_autoload_config | Loads SYSTEM\hatari\hatari.cfg on content start.  Warning.  Overrides everything except for selected TOS image. |
| System -> Atari Computer Machine Type | hatari_machinetype | Pick emulated machine.  ST, STE, TT or Falcon (Needs Restart) |
| System -> Atari Computer Ramsize | hatari_ramsize | Set amount of emulated ram.  (Needs Restart) |
| System -> TOS Image Used (Needs Restart) | hatari_tosimage | Select from list.</br>Place TOS images in system\hatari\tos\ folder.</br>Defaults to tos.img in SYSTEM folder |
| System -> Enable Fastboot | hatari_fastboot | Enable/Disable fast boot TOS patch. |
| System -> Reset Type | hatari_reset_type | Whether to Cold Start or Warm Start on "Restart". |
| Input -> Start In Mouse Mode | hatari_start_in_mouse_mode | Starts with emulated mouse active on port 1.  Otherwise joystick is active on port 1. |
| Input -> Analog Stick Mouse | hatari_mouse_control_stick | Set whether emulated mouse is controlled by left or right analog stick. |
| Input -> Emulated Mouse Speed | hatari_emulated_mouse_speed | Set the starting mouse speed from 1 to 6.  Default is 2. |
| Input -> Enable Second Joystick | hatari_twojoy | Enables a second joystick on port 2, may conflict with mouse. |
| Input -> Disable Connected Mouse | hatari_nomouse | Prevents input from your sytem mouse device. Gamepad mouse mode (select) is not disabled. |
| Input -> Disable Connected Keyboard | hatari_nokeys | Prevents input from your system keyboard. Virtual keyboard is not disabled. |
| Video -> Force Refresh Rate. | hatari_forcerefresh | Force refresh rate to Auto, NTSC 60hz or PAL 50hz.  Auto uses selected TOS rate. |
| Video -> Joy/Mouse Toggle/Speed Msg Location | hatari_joymousestatus_display | Where to display Joystick/Mouse toggle and speed change information |
| Video -> Show Drive Activity In Status Info | hatari_led_status_display | Enable to show activity in Retroarch status display |
| Media -> Fast Floppy Access | hatari_fastfdc | Decreases the time spent loading from disk. |
| Media -> Auto Insert Drive B | hatari_autoloadb | Auto inserts disk in Drive B if detected.</br>Use only for content that can use two drives.</br>M3U loads 2nd entry.  Otherwise looks for "b" as last letter before extension. |
| Media -> Write Protect Floppy Disks | hatari_writeprotect_floppy | Enable/Disable write protection for floppy disks. |
| Media -> Write Protect Hard Drives | hatari_writeprotect_hd | Enable/Disable write protection for hard drives. |
| RetroPad > Joystick Up | hatari_mapper_up | Unmapped defaults to joystick up. |
| RetroPad > Joystick Down | hatari_mapper_down | Unmapped defaults to joystick down. |
| RetroPad > Joystick Left | hatari_mapper_left | Unmapped defaults to joystick left. |
| RetroPad > Joystick Right | hatari_mapper_right | Unmapped defaults to joystick right. |
| RetroPad > A | hatari_mapper_a | Unmapped defaults to turbo fire/Mouse button 2. |
| RetroPad > B | hatari_mapper_b | Unmapped defaults to fire/mouse button 1.</br>VKBD: Press selected key. |
| RetroPad > X | hatari_mapper_x | VKBD: Toggle.  Remapping overrides VKBD toggle. |
| RetroPad > Y | hatari_mapper_y | VKBD: Toggle 'ShiftLock'. Remapping overrides VKBD function! |
| RetroPad > Select | hatari_mapper_select | Unmapped defaults to Joystick/Mouse mode toggle. |
| RetroPad > Start | hatari_mapper_start | Unmapped defaults to Enter/Exit the Hatari Settings. |
| RetroPad > L | hatari_mapper_l | Unmapped defaults to toggle the Status display. |
| RetroPad > R | hatari_mapper_r | Unmapped defaults to switch virtual keyboard page. |
| RetroPad > L2 | hatari_mapper_l2 | Unmapped defaults to decrease mouse speed. |
| RetroPad > R2 | hatari_mapper_r2 | Unmapped defaults to increase mouse speed. |
| RetroPad > L3 | hatari_mapper_l3 | n/a |
| RetroPad > R3 | hatari_mapper_r3 | Unmapped defaults to space. |
| RetroPad > Left Analog > Up | hatari_mapper_lu | Mouse mode must be off or on right analog.</br>Ignored if assigned to VKBD. |
| RetroPad > Left Analog > Down | hatari_mapper_ld | Mouse mode must be off or on right analog.</br>Ignored if assigned to VKBD. |
| RetroPad > Left Analog > Left | hatari_mapper_ll | Mouse mode must be off or on right analog.</br>Ignored if assigned to VKBD. |
| RetroPad > Left Analog > Right | hatari_mapper_lr | Mouse mode must be off or on right analog.</br>Ignored if assigned to VKBD. |
| RetroPad > Right Analog > Up | hatari_mapper_ru | Mouse mode must be off or on left analog. |
| RetroPad > Right Analog > Down | hatari_mapper_rd | Mouse mode must be off or on left analog. |
| RetroPad > Right Analog > Left | hatari_mapper_rl | Mouse mode must be off or on left analog. |
| RetroPad > Right Analog > Right | hatari_mapper_rr | Mouse mode must be off or on left analog. |

## Sharp X68000

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Menu Font Size | px68k_menufontsize | n/a |
| CPU Speed | px68k_cpuspeed | Configure the CPU speed. Can be used to slow down games that run too fast or to speed up floppy loading times. |
| RAM Size (Restart) | px68k_ramsize | Sets the amount of RAM to be used by the system. |
| Use Analog | px68k_analog | n/a |
| P1 Joypad Type | px68k_joytype1 | Set the joypad type for player 1. |
| P2 Joypad Type | px68k_joytype2 | Set the joypad type for player 2. |
| P1 Joystick Select Mapping | px68k_joy1_select | Assigns a keyboard key to joypad's SELECT button since some games use these keys as the Start or Insert Coin buttons. |
| ADPCM Volume | px68k_adpcm_vol | Sets the volume of the ADPCM sound channel. |
| OPM Volume | px68k_opm_vol | Sets the volume of the OPM sound channel. |
| Swap Disks on Drive | px68k_disk_drive | By default using the native Disk Swap interface within RetroArch's menu will swap the disk in drive FDD1. Change this option to swap disks in drive FDD0. |
| Save FDD Paths | px68k_save_fdd_path | When enabled, last loaded fdd path will be saved for each drive and then auto-loaded on startup. When disabled, FDDx starts empty. |
| Save HDD Paths | px68k_save_hdd_path | When enabled, last loaded hdd path will be saved for each drive and then auto-loaded on startup. When disabled, HDDx starts empty. |
| Rumble on FDD Reads | px68k_rumble_on_disk_read | Produces rumble effect on supported devices when reading from floppy disks. |
| Joy/Mouse | px68k_joy_mouse | Select [Mouse] or [Joypad] to control in-game mouse pointer. |
| VBtn Swap | px68k_vbtn_swap | Swaps TRIG1 and TRIG2 buttons when a 2-button gamepad is selected. |
| No Wait Mode | px68k_no_wait_mode | When set to [enabled], core runs as fast as possible. Can cause audio desync. Setting this [disabled] is recommended. |
| Push Video before Audio | px68k_push_video_before_audio | Prioritize reducing video latency over audio latency and/or stuttering. |
| Adjust Frame Rates | px68k_adjust_frame_rates | For compatibility with modern displays, slightly adjust frame rates reported to frontend in order to reduce the chances of audio stuttering.  Disable to use actual frame rates. |
| Audio Desync Hack | px68k_audio_desync_hack | Prevents audio from desynchronizing by simply discarding any audio samples generated past the requested amount per frame slice.  Forces 'No Wait Mode' to [enabled], use appropriate frontend settings to properly throttle content. |

## Microsoft MSX

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Machine Type (Restart) | bluemsx_msxtype | n/a |
| VDP Sync Type (Restart) | bluemsx_vdp_synctype | n/a |
| No Sprite Limit | bluemsx_nospritelimits | n/a |
| Sound YM2413 Enable (Restart) | bluemsx_ym2413_enable | n/a |
| Cart Mapper Type (Restart) | bluemsx_cartmapper | n/a |
| Auto Rewind Cassette | bluemsx_auto_rewind_cas | n/a |

## Sinclair ZX Spectrum

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Model (needs content load) | fuse_machine | n/a |
| Size Video Border | fuse_size_border | n/a |
| Tape Auto Load | fuse_auto_load | n/a |
| Tape Fast Load | fuse_fast_load | n/a |
| Tape Load Sound | fuse_load_sound | n/a |
| Speaker Type | fuse_speaker_type | n/a |
| AY Stereo Separation | fuse_ay_stereo_separation | n/a |
| Transparent Keyboard Overlay | fuse_key_ovrlay_transp | n/a |
| Time to Release Key in ms | fuse_key_hold_time | n/a |
| Joypad Left mapping | fuse_joypad_left | n/a |
| Joypad Right mapping | fuse_joypad_right | n/a |
| Joypad Up mapping | fuse_joypad_up | n/a |
| Joypad Down mapping | fuse_joypad_down | n/a |
| Joypad Start mapping | fuse_joypad_start | n/a |
| Joypad A button mapping | fuse_joypad_a | n/a |
| Joypad B button mapping | fuse_joypad_b | n/a |
| Joypad X button mapping | fuse_joypad_x | n/a |
| Joypad Y button mapping | fuse_joypad_y | n/a |
| Joypad L button mapping | fuse_joypad_l | n/a |
| Joypad R button mapping | fuse_joypad_r | n/a |
| Joypad L2 button mapping | fuse_joypad_l2 | n/a |
| Joypad R2 button mapping | fuse_joypad_r2 | n/a |
| Joypad L3 button mapping | fuse_joypad_l3 | n/a |
| Joypad R3 button mapping | fuse_joypad_r3 | n/a |

## IBM PC (MS-DOS)

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Force 60 FPS Output | dosbox_pure_force60fps | Enable this to force output at 60FPS. Use this if you encounter screen tearing or vsync issues. |
| Show Performance Statistics | dosbox_pure_perfstats | Enable this to show statistics about performance and framerate and check if emulation runs at full speed. |
| Save States Support | dosbox_pure_savestate | Make sure to test it in each game before using it. Complex late era DOS games might have problems.</br>Be aware that states saved with different video, CPU or memory settings are not loadable.</br>Rewind support comes at a high performance cost and needs at |
| Loading of dosbox.conf | dosbox_pure_conf | DOSBox Pure is meant to be configured via core options but optionally supports loading of legacy .conf files. |
| Use Strict Mode | dosbox_pure_strict_mode | Disable the command line, running installed operating systems and using .BAT/.COM/.EXE/DOS.YML files from the save game. |
| Advanced > Start Menu | dosbox_pure_menu_time | Set the behavior of the start menu before and after launching a game.</br>You can also force it to open by holding shift or L2/R2 when selecting 'Restart'. |
| Advanced > Input Latency | dosbox_pure_latency | By default the core operates in a high performance mode with good input latency.</br>There is a special mode available which minimizes input latency further requiring manual tweaking. |
| Advanced > Low latency CPU usage | dosbox_pure_auto_target | In low latency mode when emulating DOS as fast as possible, how much time per frame should be used by the emulation.</br>If the video is stuttering, lower this or improve render performance in the frontend (for example by disabling vsync or video proces |
| Enable On Screen Keyboard | dosbox_pure_on_screen_keyboard | Enable the On Screen Keyboard feature which can be activated with the L3 button on the controller. |
| Mouse Input Mode | dosbox_pure_mouse_input | You can disable input handling from a mouse or a touchscreen (emulated mouse through joypad will still work).</br>In touchpad mode use drag to move, tap to click, two finger tap to right-click and press-and-hold to drag |
| Bind Mouse Wheel To Key | dosbox_pure_mouse_wheel | Bind mouse wheel up and down to two keyboard keys to be able to use it in DOS games. |
| Mouse Sensitivity | dosbox_pure_mouse_speed_factor | Sets the overall mouse cursor movement speed. |
| Advanced > Horizontal Mouse Sensitivity. | dosbox_pure_mouse_speed_factor_x | Experiment with this value if the mouse is too fast/slow when moving left/right. |
| Advanced > Automatic Game Pad Mappings | dosbox_pure_auto_mapping | DOSBox Pure can automatically apply a gamepad control mapping scheme when it detects a game.</br>These button mappings are provided by the Keyb2Joypad Project (by Jemy Murphy and bigjim). |
| Advanced > Keyboard Layout | dosbox_pure_keyboard_layout | Select the keyboard layout (will not change the On Screen Keyboard). |
| Advanced > Menu Transparency | dosbox_pure_menu_transparency | Set the transparency level of the On Screen Keyboard and the Gamepad Mapper. |
| Advanced > Joystick Analog Deadzone | dosbox_pure_joystick_analog_deadzone | Set the deadzone of the joystick analog sticks. May be used to eliminate drift caused by poorly calibrated joystick hardware. |
| Advanced > Enable Joystick Timed Intervals | dosbox_pure_joystick_timed | Enable timed intervals for joystick axes. Experiment with this option if your joystick drifts. |
| Emulated Performance | dosbox_pure_cycles | The raw performance that DOSBox will try to emulate. |
| Detailed > Performance Scale | dosbox_pure_cycles_scale | Fine tune the emulated performance for specific needs. |
| Detailed > Limit CPU Usage | dosbox_pure_cycle_limit | When emulating DOS as fast as possible, how much time per frame should be used by the emulation.</br>Lower this if your device becomes hot while using this core. |
| Emulated Graphics Chip (restart required) | dosbox_pure_machine | The type of graphics chip that DOSBox will emulate. |
| CGA Mode | dosbox_pure_cga | The CGA variation that is being emulated. |
| Hercules Color Mode | dosbox_pure_hercules | The color scheme for Hercules emulation. |
| SVGA Mode (restart required) | dosbox_pure_svga | The SVGA variation that is being emulated. Try changing this if you encounter graphical glitches. |
| SVGA Memory (restart required) | dosbox_pure_svgamem | The amount of memory available to the emulated SVGA card. |
| 3dfx Voodoo Emulation | dosbox_pure_voodoo | Enables certain games with support for the Voodoo 3D accelerator.</br>3dfx Voodoo Graphics SST-1/2 emulator by Aaron Giles and the MAME team (license: BSD-3-Clause) |
| 3dfx Voodoo Performance Settings | dosbox_pure_voodoo_perf | Options to tweak the behavior of the 3dfx Voodoo emulation. |
| Memory Size (restart required) | dosbox_pure_memory_size | The amount of (high) memory that the emulated machine has. You can also disable extended memory (EMS/XMS).</br>Using more than the default is not recommended, due to incompatibility with certain games and applications. |
| Modem Type | dosbox_pure_modem | Type of emulated modem on COM1 for netplay. With the dial-up modem, one side needs to dial any number to connect. |
| CPU Type (restart required) | dosbox_pure_cpu_type | Emulated CPU type. Auto is the fastest choice.</br>Games that require specific CPU type selection:</br>- 386 (prefetch): X-Men: Madness in The Murderworld, Terminator 1, Contra, Fifa International Soccer 1994</br>- 486 (slow): Betrayal in Antara</br>- Pentium (slow): Fif |
| Advanced > CPU Core | dosbox_pure_cpu_core | Emulation method (DOSBox CPU core) used. |
| Advanced > OS Disk Modifications (restart required) | dosbox_pure_bootos_ramdisk | When running an installed operating system, modifications to the C: drive will be made on the disk image by default.</br>Setting it to 'Discard' allows the content to be closed any time without worry of file system or registry corruption.</br>When using 'Sa |
| Advanced > Free Space on D: in OS (restart required) | dosbox_pure_bootos_dfreespace | Controls the amount of free space available on the D: drive when running an installed operating system.</br>If the total size of the D: drive (data + free space) exceeds 2 GB, it can't be used in earlier versions of Windows 95.</br>WARNING: Created save fil |
| Advanced > Force Normal Core in OS | dosbox_pure_bootos_forcenormal | The normal core can be more stable when running an installed operating system.</br>This can be toggled on and off to navigate around crashes. |
| Audio Sample Rate (restart required) | dosbox_pure_audiorate | This should match the frontend audio output rate (Hz) setting. |
| SoundBlaster Settings | dosbox_pure_sblaster_conf | Set the address, interrupt, low 8-bit and high 16-bit DMA. |
| MIDI Output | dosbox_pure_midi | Select the .SF2 SoundFont file, .ROM file or interface used for MIDI output.</br>To add SoundFonts or ROM files, copy them into the 'system' directory of the frontend.</br>To use the frontend MIDI driver, make sure it's set up correctly. |
| Advanced > SoundBlaster Type | dosbox_pure_sblaster_type | Type of emulated SoundBlaster card. |
| Advanced > SoundBlaster Adlib/FM Mode | dosbox_pure_sblaster_adlib_mode | The SoundBlaster emulated FM synth mode. All modes are Adlib compatible except CMS. |
| Advanced > SoundBlaster Adlib Provider | dosbox_pure_sblaster_adlib_emu | Provider for the Adlib emulation. Default has good quality and low performance requirements. |
| Advanced > Enable Gravis Ultrasound (restart required) | dosbox_pure_gus | Enable Gravis Ultrasound emulation. Settings are fixed at port 0x240, IRQ 5, DMA 3.</br>If the ULTRADIR variable needs to be different than the default 'C:\ULTRASND' you need to issue 'SET ULTRADIR=...' in the command line or in a batch file. |
| Advanced > Swap Stereo Channels | dosbox_pure_swapstereo | Swap the left and the right audio channel. |

## ScummVM

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Auto performance tuner | scummvm_auto_performance_tuner | In-game automatic change of timing/frameskip settings if low performances are detected. Timing/frameskip settings will be changed in sequence, if audio buffer underruns are detected and for the current game session only, and restored in sequence if  |
| Cursor > Exclusive cursor control with RetroPad | scummvm_gamepad_cursor_only | Allows the use of RetroPad only to control mouse cursor, excluding the other inputs (e.g. physical mouse, touch screen). |
| Cursor > Gamepad Cursor Speed | scummvm_gamepad_cursor_speed | Sets the mouse cursor speed multiplier when moving the cursor with the RetroPad left analog stick or D-Pad. The default value of '1.0' is optimised for games that have a native resolution of '320x200' or '320x240'. When running 'high definition' gam |
| Cursor > Gamepad Cursor Acceleration | scummvm_gamepad_cursor_acceleration_time | The amount of time (In seconds) it takes for the cursor to reach full speed |
| Cursor > Analog Cursor Response | scummvm_analog_response | Determines how the speed of the cursor varies when tilting the RetroPad left analog stick. 'Linear': Speed is directly proportional to analog stick displacement. This is standard behaviour with which most users will be familiar. 'Quadratic': Speed i |
| Cursor > Analog Deadzone | scummvm_analog_deadzone | Sets the deadzone in percentage of the RetroPad analog sticks. Used to eliminate cursor drift/unwanted input. |
| Cursor > Mouse Speed | scummvm_mouse_speed | Sets the mouse cursor speed multiplier when moving the cursor with the RetroMouse. |
| Cursor > Mouse Fine Control Speed Reduction | scummvm_mouse_fine_control_speed_reduction | Sets the mouse cursor speed reduction as percentage of normal speed when fine control is activated. |
| Timing > Allow Timing Inaccuracies | scummvm_allow_timing_inaccuracies | Allow timing inaccuracies that reduces CPU requirements. Though most timing deviations are imperceptible, in some cases it may introduce audio sync/timing issues, hence this option should be enabled only if full speed cannot be reached otherwise. |
| Timing > Frame rate cap | scummvm_framerate | Set core frame rate upper limit. Changing this setting will reset the core. |
| Timing > Sample rate | scummvm_samplerate | Set core sample rate. Changing this setting will reset the core. |
| RetroPad > Up | scummvm_mapper_up | n/a |
| RetroPad > Down | scummvm_mapper_down | n/a |
| RetroPad > Left | scummvm_mapper_left | n/a |
| RetroPad > Right | scummvm_mapper_right | n/a |
| RetroPad > A | scummvm_mapper_a | n/a |
| RetroPad > B | scummvm_mapper_b | n/a |
| RetroPad > X | scummvm_mapper_x | n/a |
| RetroPad > Y | scummvm_mapper_y | n/a |
| RetroPad > Select | scummvm_mapper_select | n/a |
| RetroPad > Start | scummvm_mapper_start | n/a |
| RetroPad > L | scummvm_mapper_l | n/a |
| RetroPad > R | scummvm_mapper_r | n/a |
| RetroPad > L2 | scummvm_mapper_l2 | n/a |
| RetroPad > R2 | scummvm_mapper_r2 | n/a |
| RetroPad > L3 | scummvm_mapper_l3 | n/a |
| RetroPad > R3 | scummvm_mapper_r3 | n/a |
| RetroPad > Left Analog > Up | scummvm_mapper_lu | n/a |
| RetroPad > Left Analog > Down | scummvm_mapper_ld | n/a |
| RetroPad > Left Analog > Left | scummvm_mapper_ll | n/a |
| RetroPad > Left Analog > Right | scummvm_mapper_lr | n/a |
| RetroPad > Right Analog > Up | scummvm_mapper_ru | n/a |
| RetroPad > Right Analog > Down | scummvm_mapper_rd | n/a |
| RetroPad > Right Analog > Left | scummvm_mapper_rl | n/a |
| RetroPad > Right Analog > Right | scummvm_mapper_rr | n/a |

## Alpha Player

| Setting                               | Key            | Info           |
| ------------------------------------- | -------------- | -------------- |
| Resolution (restart) | mplayer_video_resolution | n/a |
| Hardware Decoder (restart) | mplayer_hw_decoder | n/a |
| Loop | mplayer_loop_content | n/a |
| Software Decoder Threads (restart) | mplayer_sw_decoder_threads | n/a |
| Colorspace | mplayer_color_space | n/a |
| Visualizer Resolution | mplayer_fft_resolution | n/a |