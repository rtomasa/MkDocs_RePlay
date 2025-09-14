# Common Issues

| Problem                                      | Solution       |
| -------------------------------------------- | -------------- |
| The system does not boot up or boot up displaying many errors | 1. Verify that the RePlay OS IMG file was correctly written to the SD card by rewriting it.</br>2. If the issue persists, reduce the value of the `arm_freq` parameter in the `/boot/firmware/config.txt` file.</br>3. If the issue persists, try using a different SD card to discard corruption or damage in the current one. |
| My gamepad or joystick does not work or is not recognised | Please check [New Controllers Support](mappings.md) from the advanced Wiki section |
| PSX PAL games display black screen | This is a SwanStation bug. The workaround is changing `System Settings > Display Settings > Crop Mode > All Borders` and then `Save Game Settings` |
| Games run poorly with many slowdowns, but I recall them working fine some time ago. | The issue is most likely that you are using a very weak power adapter. Please use an official power supply or a compatible one with a voltage of 5.1V to 5.25V. |
| My wireless controllers stop working when I connect an external USB 3 device | USB 3 can cause 2.4 GHz interference, which disrupts other wireless devices |