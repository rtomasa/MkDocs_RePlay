# Raspberry Pi 3/4 Audio Jack

On Raspberry Pi 3 and 4 models, the built-in audio jack is **disabled by default**. This is because enabling it will disable HDMI audio, USB DACs, and GPIO-based audio devices.
Additionally, the integrated audio jack on these models only offers **11-bit audio quality**, which is noticeably lower than other available outputs.

If you still wish to enable the audio jack, follow these steps:

1. Open `/boot/firmware/config.txt` in a text editor.
2. Set the line:
```
dtparam=audio=on
```
3. Reboot your Raspberry Pi.
4. In the system audio settings, set the output device to **GPIO**.