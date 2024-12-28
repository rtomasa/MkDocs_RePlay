# Input Lag

Different systems natively have varying amounts of input lag, introducing some delay between user input and the display. Emulation can add additional latency, particularly due to how video is managed. RePlay OS is developed to minimize input lag and provide the best experience, even on weaker devices like the Raspberry Pi 3.

By default, the video engine used by RePlay OS introduces a maximum of 1 frame of input lag while maintaining a balanced performance. A special option, available in `REPLAY OPTIONS > SYSTEM > EMULATION QUALITY`, allows users to choose different levels of input lag and sound quality:

* `LOW`: Uses the standard video latency engine and a linear sound resampler.
* `MEDIUM`: Uses the standard video latency engine and a sync sound resampler.
* `HIGH`: Uses the reduced video latency engine and a sync sound resampler.

## About the Different Video Latency Engines

* **Standard Mode**: Introduces up to 1 frame of latency and offers the best performance. Recommended for most scenarios.
* **Reduced Mode**: Provides a zero-lag experience but requires a relatively powerful CPU, depending on the emulated system. This option works perfectly fine with many 8-bit and 16-bit systems, even on a Raspberry Pi 3.

    **NOTE:** reduced latency mode does not uses any kind of run-ahead technique, so it is 100% compatible with all system cores.

    **IMPORTANT:** If you experience sound issues, such as stuttering, while using reduced latency mode, switch to the standard profile. These issues can occur due to the high CPU demands of reduced latency mode.

## About the Different Sound Resampler Engines

* **Linear Resampler**: The fastest resampler, minimizing CPU requirements while providing very good sound quality.
* **Sync Resampler**: The most advanced resampler engine, delivering the best sound quality but requiring more CPU resources.

## USB Gamepads & Joysticks Latency

By default, RePlay OS is preconfigured with a 1ms polling rate, ensuring ultra-fast response times for optimal gaming performance.