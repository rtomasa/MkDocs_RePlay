# Common Issues

| Problem                                      | Solution       |
| -------------------------------------------- | -------------- |
| The system does not boot up or boot up displaying many errors | 1. Verify that the RePlayOS IMG file was correctly written to the SD card by rewriting it.</br>2. If the issue persists, reduce the value of the `arm_freq` parameter in the `/boot/firmware/config.txt` file.</br>3. If the issue persists, try using a different SD card to discard corruption or damage in the current one. |
| My gamepad or joystick does not work or is not recognised | Please check [New Controllers Support](mappings.md) from the advanced Wiki section |
| Games run poorly with many slowdowns, but I recall them working fine some time ago. | The issue is most likely that you are using a very weak power adapter. Please use an official power supply or a compatible one with a voltage of 5.1V to 5.25V. |
| HDMI-0 port is faulty and I need to use HDMI-1 as the main output | Add the `nohdmi0` option to the `dtoverlay` line in `/boot/firmware/config.txt` (for example `dtoverlay=vc4-kms-v3d,nohdmi0`) and reboot the system. |
| My wireless controllers stop working when I connect an external USB 3 device | USB 3 can cause 2.4 GHz interference, which disrupts other wireless devices |
| Interlaced video shakes heavily when using DPI (GPIO) output | Please refer to [EEPROM Update](eeprom.md) section for instructions |
