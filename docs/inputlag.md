# Input Lag

Different systems natively have varying amounts of input lag, introducing some delay between user input and the display. Emulation can add additional latency, particularly due to how video is managed. RePlayOS is developed to minimize input lag and provide the best experience, even on weaker devices like the Raspberry Pi 3.

By default, the video engine used by RePlayOS introduces zero-lag without impacting the performance.

## USB Gamepads/Joysticks & GPIO Joystics Latency

By default, RePlayOS is configured with a 1 ms polling rate, ensuring ultra-fast response times for optimal gaming performance.

In addition, RePlayOS uses a bitmask input engine for digital controllers, which provides the following input-lag benefits:

* **Consistent snapshot**: All button states are captured in the same poll cycle, eliminating per-button timing skew and matching real hardware behavior.
* **Reduced input latency**: Cores skip dozens of callback round trips per frame. The improvement is small but measurable compared to traditional per-button polling.
