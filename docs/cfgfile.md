# RePlay Options File

The following is a description of all available options and default values that RePlay uses for global configuration.

The configuration file is located in `/media/sd/config/replay.cfg`:

```cfg
# video_connector
## 0 = hdmi
## 1 = dpi (used for gpio)
video_connector             = "0"
# video_mode
## NRR (Native Refresh Rate)
## 0 = default
## 1 = crt 320x240@nrr (ui boots @60)
## 2 = crt 320x240@nrr (ui boots @50)
## 3 = lcd native resolution & nrr
## 4 = lcd 1920x1080@60
## 5 = lcd 1280x720@60
## 6 = lcd 1280x1024@60
## 7 = lcd 1024x768@60
## 8 = lcd 2560x1440@60
## 9 = lcd 3840x2160@60
video_mode                  = "0"
# video_monitor_multi_mode
## 0 = disabled
## 1 = dual cloned
## 2 = dual horizontal
## 3 = dual vertical
## 4 = dual smart rotation
video_monitor_multi_mode     = "0"
# video_lcd_type
## generic_60 = supports 55-61hz ranges
## gaming_vrr = supports 48-75hz ranges
video_lcd_type              = "generic_60"
# video_crt_type
## generic_15
## arcade_15
## arcade_15_25
## arcade_15_25_31
## arcade_31 (also used for PC)
video_crt_type              = "generic_15"
# video_crt_csync_mode (requires RGB-Pi compatible hardware)
## 0 = AND
## 1 = XOR
## 2 = separated H/V
video_crt_csync_mode        = "0"
# video_crt_rgb_range
## 0 = auto
## 1 = full (0:255)
## 2 = limited (16:235)
video_crt_rgb_range         = "0"
# video_aspect_ratio
## 0 = full screen 4:3
## 1 = full screen native
## 2 = vertical integer scaling, horizontal 4:3
## 3 = vertical integer scaling, horizontal native
## 4 = horizontal integer scaling, vertical 4:3
## 5 = horizontal integer scaling, vertical native
## 6 = full integer scaling
## 7 = full integer over scaling (only FHD TVs)
## 8 = full integer under scaling
video_aspect_ratio          = "0"
# video_crt_h_shift
## values = -16<-->16
video_crt_h_shift           = "0"
# video_crt_h_size
## values = 0.5<-->1.5
video_crt_h_size            = "1.0"
video_monitor_x             = "0"
video_monitor_y             = "0"
# video_gamma
## values = 0.5<-->1.5
video_gamma                 = "1.0"
# video_red_scale
## values = 0.0<-->1.0
video_red_scale             = "1.0"
# video_green_scale
## values = 0.0<-->1.0
video_green_scale           = "1.0"
# video_blue_scale
## values = 0.0<-->1.0
video_blue_scale            = "1.0"
# video_ui_rotation_mode
## 0 = 0
## 1 = 90
## 2 = 180
## 3 = 270
video_ui_rotation_mode      = "0"
video_show_fps              = "false"
video_show_info             = "false"
# video_filter
## 0 = none
## 1 = light scanlines
## 2 = medium scanlines
## 3 = strong scanlines
## 4 = black scanlines          
video_filter                = "0"
video_ambiscan              = "true"
# video_screen_saver
## 0 = OFF
## 60000 = 1 min
## 180000 = 3 min
## 300000 = 5 min
## 600000 = 10 min
## 900000 = 15 min
video_screen_saver          = "0"
# audio_card
## 0 = HDMI
## 1 = USB DAC
## 2 = GPIO DAC
video_hdmi_cec              = "false"
audio_card                  = "0"
audio_mono                  = "false"
audio_normalization         = "false"
# audio_system_volume
## values = 0<-->10
audio_system_volume         = "10"
# input_gcon2_flash
## 0 = disabled
## 1 = pulse
## 2 = hold
input_gcon2_flash           = "1"
input_gcon2_offscreen       = "true"
input_ui_swap_ab            = "false"
input_all_control_ui        = "false"
input_ui_select_fav         = "false"
# input_ui_menu_btn
## 0 = home button
## 1 = select+start
## 2 = hold start
input_ui_menu_btn           = "1"
# input_true_kbd
## true = keyboard works in native scancode mode
## false = keyboard works in special cmd event mode
input_true_kbd              = "true"
system_coinop               = "false"
# system_coinop_time
## game time you get for a credit
system_coinop_time          = "180"
# system_verbose
## 0 = debug
## 1 = info
## 2 = warn
## 3 = error
## 4 = trace
## 5 = disabled
system_verbose              = "5"
system_kiosk_mode           = "false"
# system_emu_quality
## 0 = Performance
##     - audio linear resampler
##     - set specific core options
## 1 = Balanced
##     - audio sync resampler
##     - set specific core options
## 2 = Quality
##     - audio sync resampler
##     - set specific core options
system_emu_quality          = "1"
# system_low_latency_mode
## true = -1/0 frames input lag
## false = 0/1 frames input lag
system_low_latency_mode     = "false"
# system_skin
## 0 = replay (default)
## 1 = mega tech
## 2 = play choice
## 3 = astro
## 4 = super video
## 5 = mvs
## 6 = rpg
## 7 = fantasy
## 8 = simple purple
## 9 = metal
## 10 = unicolors
## 11-36 = for custom user skins
system_skin                 = "0"
# system_boot_to_system
## all
## arcade_fbneo
## arcade_mame
## arcade_mame_2k3p
## arcade_dc
## nintendo_nes
## nintendo_snes
## nintendo_gb
## sega_smd
## sony_psx
system_boot_to_system       = "all"
# system_storage
## sd = internal sd card
## usb = external usb drive
## nfs = network nfs share
system_storage              = "sd"
system_ui_pauses_core       = "false"
system_folder_regen         = "true"
# view_players
## 0 = show all
## 1-6 = num players
view_players                = "0"
# view_rotation
## 0 = show all
## 1 = horizontal
## 2 = vertical
view_rotation               = "0"
# view_displays
## 0 = show all
## 1 = single screen
## 2 = dual screen
view_displays               = "0"
# view_buttons
## 0 = show all
## 1-6 = N or less buttons
view_buttons                = "0"
view_player                 = "true"
view_arcade                 = "true"
view_console                = "true"
view_computer               = "true"
view_handheld               = "true"
nfs_server                  = "192.168.X.X"
nfs_share                   = "/export/share"
wifi_name                   = "MyWifi"
wifi_pwd                    = "********"
wifi_country                = "ES"
# wifi_mode
## wpa2
## wpa3
## transition (for mixed wpa2 & wpa3)
wifi_mode                   = "transition"
wifi_hidden                 = "false"
# addon_retroflag_case_pi5
## 0 = disabled
## 1 = reset button for reboot
## 2 = reset button for menu
addon_retroflag_case_pi5    = "0"
# addon_tilt_input_pi5
## 0 = disabled
## 1 = +90
## 3 = +270
addon_tilt_input_pi5        = "0"
addon_gpio_joy_pi5          = "0"
addon_dpi_dac_pi5           = "0"
```