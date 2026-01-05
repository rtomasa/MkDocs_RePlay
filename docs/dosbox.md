# DOSBox

DOSBox uses a special `DOSBoxPureMidiCache.txt` configuration file in your BIOS folder to set MIDI sound fonts.
The RePlayOS official BIOS pack provides a standard file structure already configured to support all required sound fonts.
These sound fonts are shared with ScummVM to save space and avoid duplicated files.
If you want to use additional sound fonts, you can either modify the configuration file below or delete it so DOSBox will scan for `.sf2` files on the next boot and generate a new configuration file.

## Recommended DOSBoxPureMidiCache.txt configuration file

```cfg
scummvm/extra/CM32L_CONTROL.ROM
Roland MT-32/CM-32L: CM32L
scummvm/extra/MT32_CONTROL.ROM
Roland MT-32/CM-32L: MT32
scummvm/soundfonts/Roland_SC-55.sf2
General MIDI: Roland_SC-55
scummvm/soundfonts/GM_Roland.sf2
General MIDI: GM_Roland
scummvm/soundfonts/FluidR3_GM.sf2
General MIDI: FluidR3_GM
scummvm/soundfonts/UHD3.sf2
General MIDI: UHD3
```

## About General MIDI music

By using the above configuration, the system will automatically use Roland SC-55 music when the [additional required BIOS files](addbios.md#minimum-bios-system-files) are present and the game supports it. No additional configuration is required.

## About Roland MT-32 music

By using the above configuration, the system will automatically use Roland MT-32 music when the [additional required BIOS files](addbios.md#minimum-bios-system-files) are present and the game supports it. No additional configuration is required.