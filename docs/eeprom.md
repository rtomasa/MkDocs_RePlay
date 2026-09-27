RePlayOS supports analog video through the DPI interface (GPIO). To ensure proper operation—especially when using interlaced video modes—a minimum Raspberry Pi EEPROM/firmware version is required on Raspberry Pi 4 and Raspberry Pi 5 devices (the fix is not available for Raspberry Pi 3).

RePlayOS checks the installed EEPROM version and shows a warning when it is below the minimum required release (2025-11-05). The public image does not install EEPROM updates automatically; update it deliberately using the Raspberry Pi tools below when required.

Pi 3 has no applicable bootloader EEPROM. On Pi 4/5, back up important data before updating and perform a cold boot (disconnect and reconnect power) after the update.

## Check EEPROM version & apply optional configurations

```sh
vcgencmd bootloader_version
```

Expected output example:

```
2025/11/05 17:37:18
version 57db150d63864d47e6c9071f6b086a5401eb4e92 (release)
timestamp 1762364238
update-time 1762770986
capabilities 0x0000007f
```

If the EEPROM date is **>= 2025/11/05**, your firmware is already compatible.
If you want to apply RePlayOS custom optimizations to speed up the boot process, run:

```sh
rpi-eeprom-config --edit
```

Add or modify the following settings:

```ini
POWER_OFF_ON_HALT=1
NET_INSTALL_ENABLED=0
NET_INSTALL_AT_POWER_ON=0
```

You can verify the active configuration at any time with:

```sh
rpi-eeprom-config
```

## Manual EEPROM update – Raspberry Pi 4 family

```sh
/usr/bin/rpi-eeprom-update -d -f /usr/lib/firmware/raspberrypi/bootloader-2711/latest/pieeprom-2025-11-05-replay.bin
poweroff
```

Disconnect and reconnect the power cable to complete the installation.

## Manual EEPROM update – Raspberry Pi 5 family

```sh
/usr/bin/rpi-eeprom-update -d -f /usr/lib/firmware/raspberrypi/bootloader-2712/latest/pieeprom-2025-11-05-replay.bin
poweroff
```

Disconnect and reconnect the power cable to complete the installation.
