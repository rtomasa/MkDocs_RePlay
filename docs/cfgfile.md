# RePlay Options File

The following is a description of all available options and default values that RePlay uses for global configuration.

The configuration file is located in `/media/sd/config/replay.cfg`:

```ini
# video_mode
## 0 = default
## 1 = crt 320x240@vrr
## 2 = crt 640x480@vrr
## 3 = lcd 1920x1080@60
## 4 = lcd 1280x720@60
## 5 = lcd 1280x1024@60
## 6 = lcd 1024x768@60
## 7 = lcd 1440x1440@90
## 8 = lcd 1920x1080@60/50
## 9 = lcd 1280x720@60/50
video_mode                  = "0"
# video_monitor_dual_mode
## 0 = disabled
## 1 = duplicate
## 2 = horizontal
## 3 = vertical
video_monitor_dual_mode     = "0"
# video_crt_type
## generic_15
## arcade_15
## arcade_31
## arcade_15_25
## arcade_15_25_31
## pc_31_120
video_crt_type              = "generic_15"
# video_aspect_ratio
## 0 = automatic
## 1 = forced 4:3 (full screen)
## 2 = pixel perfect (integer scaling)
## 3 = system native (full screen)
## 4 = over scaled (integer scaling)
## 5 = under scaled (integer scaling)
video_aspect_ratio          = "0"
video_monitor_x             = "0"
video_monitor_y             = "0"
video_ui_init_refresh_rate  = "60"
# video_ui_rotation_mode
## 0 = 0
## 1 = 90
## 2 = 180
## 3 = 270
video_ui_rotation_mode      = "0"
video_overscan_reduction    = "false"
video_show_fps              = "false"
video_show_info             = "false"
# video_color_blind
## 0 = none
## 1 = protanopia
## 2 = deuteranopia
## 3 = tritanopia
video_color_blind           = "0"
# video_filter
## 0 = none
## 1 = subtle scanlines
## 2 = strong scanlines
video_filter                = "0"
# video_screen_saver_delay
## 0 = OFF
## 60000 = 1 min
## 180000 = 3 min
## 300000 = 5 min
## 600000 = 10 min
## 900000 = 15 min
video_screen_saver_delay    = "60000"
audio_card                  = "1"
audio_mono                  = "false"
# audio_system_volume
## values = 0-10
audio_system_volume         = "10"
input_analog_to_digital     = "true"
# input_digital_to_analog
## 0 = off
## 1 = 1/2 (b/x)
## 2 = 2/3 (x/y)
## 3 = 9/10 (shoulders l/r)
input_digital_to_analog     = "0"
input_gcon2_screen_flash    = "true"
input_ui_swap_ab            = "false"
input_ui_select_fav         = "false"
# input_ui_menu_btn
## 0 = home button
## 1 = select+start
## 2 = hold start
input_ui_menu_btn           = "1"
# system_ui_view_filter
## 0 = show all
## 1 = show only horizontal
## 2 = show only vertical
## 3 = show only side-by-side dual screen 
## 4 = show only stacked dual screen
system_ui_view_filter       = "0"
system_ui_view_player       = "false"
system_ui_view_arcade       = "true"
system_ui_view_console      = "true"
system_ui_view_computer     = "true"
system_ui_view_handheld     = "true"
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
## 0 = Performance
##     - video triple-buffer
##     - audio linear resampler
##     - set specific core options
## 1 = Balanced
##     - video triple-buffer
##     - audio sync resampler
##     - set specific core options
## 2 = Quality
##     - video double-buffer
##     - audio sync resampler
##     - set specific core options
system_emu_quality          = "1"
# system_skin
## 0 = blue (default)
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
system_storage_safe_mode    = "true"
nfs_server                  = "192.168.x.x"
nfs_share                   = "/media/share"
```