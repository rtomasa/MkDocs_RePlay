# Common Issues

| Problem                                      | Solution       |
| -------------------------------------------- | -------------- |
| The system does not boot up or boot up displaying many errors | 1. Verify that the RePlayOS IMG file was correctly written to the SD card by rewriting it.</br>2. If the issue persists, reduce the value of the `arm_freq` parameter in the `/boot/firmware/config.txt` file.</br>3. If the issue persists, try using a different SD card to discard corruption or damage in the current one. |
| My gamepad or joystick does not work or is not recognised | Please check [New Controllers Support](mappings.md) from the advanced Wiki section |
| Games run poorly with many slowdowns, but I recall them working fine some time ago. | You are probably using a very weak power adapter. Please use an official power supply or a compatible one with a voltage of 5.1V to 5.25V. |
| HDMI-0 port is faulty and I need to use HDMI-1 as the main output | Add the `nohdmi0` option to the `dtoverlay` line in `/boot/firmware/config.txt` (for example `dtoverlay=vc4-kms-v3d,nohdmi0`) and reboot the system. |
| My wireless controllers stop working when I connect an external USB 3 device | USB 3 can cause 2.4 GHz interference, which disrupts other wireless devices |
| Interlaced video shakes heavily when using DPI (GPIO) output | Please refer to [EEPROM Update](eeprom.md) section for instructions |
| RePlayOS fails to download updates and/or auto detect time zone | Your ISP is blocking the NTP time server. You can update the date manually via SSH using this sample command: `date -s "25 APR 2026 16:40:00"` |

| Load State Errors                            | Description       |
| -------------------------------------------- | -------------- |
| `ERR-001` | failed to build the savestate file path/name before loading. |
| `ERR-004` | failed to seek the savestate file. |
| `ERR-005` | failed to read the savestate file size. |
| `ERR-006` | savestate file size does not match what the core expects. |
| `ERR-007` | failed to allocate memory for the load buffer. |
| `ERR-008` | failed to read the full savestate data from disk. |
| `ERR-009` | the core rejected the savestate during unserialize/load. |

| Save State Errors                            | Description       |
| -------------------------------------------- | -------------- |
| `ERR-001` | savestates are not supported because the core reports a serialize size of zero. |
| `ERR-002` | savestates are not supported because the core failed `retro_serialize`. |
| `ERR-003` | failed to build the savestate file path/name before saving. |
| `ERR-004` | failed to allocate memory for the save buffer. |
| `ERR-005` | failed to open the savestate file for writing. |
| `ERR-006` | short write while saving; not all savestate data was written. |