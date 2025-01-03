# Common Issues

| Problem                                      | Solution       |
| -------------------------------------------- | -------------- |
| Bad D-Pad/Analog Stick Behavior in N64 Games | Disable *Left Stick to DPad* option whether from ```RePlay Options > Input > Left Stick to DPad``` for global configuration or ```System Menu > System Input > Left Stick to DPad``` for specific System/Game configuration |
| The system does not boot up or boot up displaying many errors | 1. Verify that the RePlay OS IMG file was correctly written to the SD card by rewriting it.</br>2. If the issue persists, reduce the value of the `arm_freq` parameter in the `/boot/firmware/config.txt` file.</br>3. If the issue persists, try using a different SD card to discard corruption or damage in the current one. |
| My gamepad or joystick does not work or is not recognised | Please check [New Controllers Support](mappings.md) from the advanced Wiki section |