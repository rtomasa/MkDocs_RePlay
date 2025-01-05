# Emulation Profiles

Different systems offer emulation options designed to enhance accuracy, improving game visuals, sound, latency, and eliminating emulation bugs. However, higher levels of emulation precision often require increased CPU and GPU resources.

RePlay includes the `REPLAY OPTIONS > SYSTEM > EMULATION PROFILE` feature, which automatically adjusts core settings to provide optimal performance for different scenarios. This feature considers emulation quality, latency, and the specific Raspberry Pi model in use, ensuring the best out-of-the-box experience for all users. Below are the supported profile modes:

### Supported Profile Modes

- **`PERFORMANCE`**: Optimized for maximum performance, using high-level emulation (HLE) options and a linear sound resampler.  
- **`BALANCED`**: Offers a well-rounded balance between performance and accuracy, employing HLE options and a sync sound resampler.  
- **`QUALITY`**: Focuses on maximum accuracy, utilizing low-level emulation (LLE) options and a sync sound resampler.  

## About the Different Sound Resampler Engines

- **Linear Resampler**: The fastest resampler, requiring minimal CPU resources while delivering good sound quality.  
- **Sync Resampler**: A more advanced resampler engine that provides superior sound quality but demands higher CPU resources.

# Supported Systems

Currently, this option applies sound resampler settings to all cores and automatically manages configurations for the following systems:

- **Nintendo 64**  
- **SEGA Dreamcast** (including both console and arcade versions)