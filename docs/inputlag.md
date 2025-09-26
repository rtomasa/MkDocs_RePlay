# Input Lag

Different systems natively have varying amounts of input lag, introducing some delay between user input and the display. Emulation can add additional latency, particularly due to how video is managed. RePlay OS is developed to minimize input lag and provide the best experience, even on weaker devices like the Raspberry Pi 3.

By default, the video engine used by RePlay OS introduces near zero-lag while maintaining a good performance. A special option, available in `REPLAY OPTIONS > SYSTEM > LOW LATENCY MODE`, allows users to choose different levels of input lag:

* `OFF`: uses the standard video latency engine achieving 0 to 1 frames of input lag with the best performance.
* `ON`: uses the reduced video latency engine achieving -1 to 0 frames of input lag.

**NOTE:** reduced latency mode does not uses any kind of run-ahead technique, so it is 100% compatible with all system cores.

## USB Gamepads/Joysticks & GPIO Joystics Latency

By default, RePlay OS is configured with a 1 ms polling rate, ensuring ultra-fast response times for optimal gaming performance.

In addition, RePlay OS uses a bitmask input engine for digital controllers, which provides the following input-lag benefits:

* **Consistent snapshot**: All button states are captured in the same poll cycle, eliminating per-button timing skew and matching real hardware behavior.
* **Reduced input latency**: Cores skip dozens of callback round trips per frame. The improvement is small but measurable compared to traditional per-button polling.
