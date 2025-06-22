# Alpha Player

**Alpha Player** is a multimedia core for RePlay OS, based on a port of the powerful FFmpeg audio/video decoding library to the libretro platform. This allows seamless playback of a wide variety of audio and video formats, along with advanced features like audio visualizations and smooth interframe blending for non-native framerates.

---

## Features

* **Wide format support:** Thanks to FFmpeg, supports most common video and audio file formats (MKV, MP4, AVI, MP3, FLAC, OGG, WAV, M4A, etc.)
* **Audio Visualizer:** Displays a real-time FFT-based audio visualizer when playing music.
* **Interframe Blending:** Enables smoother playback for videos with non-native framerates.
* **Playlist Support:** Play M3U playlists with track navigation.
* **Subtitle Support:** Toggle subtitle tracks and display them in video playback.
* **Audio Track Selection:** Easily switch between multiple audio tracks in supported media.
* **Custom Loop Modes:** Supports track repeat, loop all, and shuffle for playlists.
* **On-Screen Progress and Info:** Quick access to current time, progress, and media info.

---

## Usage Notes

> **Note:**
> Alpha Player is focused on Raspberry Pi devices and is actively developed for RePlay OS.
> It is *not guaranteed* to work on other platforms or general Linux systems.

---

## Controls

| Button | Action                         |
| :----- | :----------------------------- |
| START  | Play/Pause                     |
| A      | Display current progress/time  |
| B      | Display media title            |
| X      | Enable/disable video subtitles |
| Y      | Change audio track             |
| L      | Previous track (M3U)           |
| R      | Next track (M3U)               |
| LEFT   | Seek -15s                      |
| RIGHT  | Seek +15s                      |
| UP     | Seek +3min (180s)              |
| DOWN   | Seek -3min (180s)              |
| L2     | Seek -5min (300s)              |
| R2     | Seek +5min (300s)              |

---

## Supported Formats

* Video: `.mkv`, `.avi`, `.mp4`, `.mov`, `.flv`, `.wmv`, `.webm`, `.mpeg`, `.mpg`, `.m2ts`, `.vob`, etc.
* Audio: `.mp3`, `.flac`, `.ogg`, `.m4a`, `.wav`, `.wma`, etc.
* Playlists: `.m3u`
* (Full list matches [libretro FFmpeg core formats](https://docs.libretro.com/library/ffmpeg/))

---

## Project Origins and License

* **Based on:** [libretro FFmpeg core](https://docs.libretro.com/library/ffmpeg/), authored by Fabrice Bellard and the FFmpeg team.
* **Reworked and ported by:** Rubén Tomás (RTA)
* **Notes:** The codebase has been heavily refactored and reorganized to separate it from RetroArch’s internal version.

---

## Changelog

**v2.1.0**

* Changed scaling from POINT to BILINEAR for improved image quality
* Fixed seeking functionality
* Fixed random crash when changing audio tracks

**v2.0.4**

* Reverted changes from v2.0.2 that caused video issues

**v2.0.3**

* Added audio gain for videos with 5.1 channel audio tracks

**v2.0.2**

* Fixed crash when seeking in many videos

**v2.0.1**

* Fixed crash with music containing embedded images in GIF/BMP format

**v2.0.0**

* Major update to modern FFmpeg and libretro APIs
* Added playlist support, loop/shuffle modes, new debug flags, improved OSD info, audio visualizer resolution options, and more

---

## Known Issues / TODO

* Playback of videos using non-standard timings (e.g. 288p PAL 60Hz) on CRTs may not work correctly.

---

## Further Information

* [libretro FFmpeg core documentation](https://docs.libretro.com/library/ffmpeg/)
* [Original core README on GitHub](https://github.com/libretro/docs/blob/master/docs/library/ffmpeg.md)
