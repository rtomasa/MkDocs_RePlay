# Adding BIOS

Many systems require some mandatory BIOS files to run or use some special configurations. You can copy your BIOS files into the corresponding `/bios` folder in your storage unit.

**IMPORTANT:** RePlayOS will check for any missing BIOS files required by the system you are trying to use. If any BIOS file is missing, it will prevent you from loading games until you copy all required BIOS files.

## Minimum BIOS System Files

The following table is a reference about the minimum required BIOS files used by the different systems in RePlayOS:

**NOTE:** please check the [full BIOS folder structure](#full-bios-file-structure) in case that some system is not properly booting with the minimum bios files.


| System             | BIOS File                              |
|--------------------|----------------------------------------|
| arcade_dc          | dc/airlbios.zip                        |
| arcade_dc          | dc/awbios.zip                          |
| arcade_dc          | dc/dc_boot.bin                         |
| arcade_dc          | dc/f355.zip                            |
| arcade_dc          | dc/f355bios.zip                        |
| arcade_dc          | dc/f355dlx.zip                         |
| arcade_dc          | dc/hod2bios.zip                        |
| arcade_dc          | dc/naomi.zip                           |
| arcade_dc          | dc/naomi2.zip                          |
| arcade_dc          | dc/segasp.zip                          |
| atari_5200         | 5200.rom                               |
| atari_7800         | 7800 BIOS (U).rom                      |
| atari_lynx         | lynxboot.img                           |
| commodore_ami      | capsimg.so                             |
| commodore_ami      | kick33180.A500                         |
| commodore_ami      | kick34005.A500                         |
| commodore_ami      | kick37175.A500                         |
| commodore_ami      | kick37350.A600                         |
| commodore_ami      | kick40063.A600                         |
| commodore_ami      | kick39106.A1200                        |
| commodore_ami      | kick40068.A1200                        |
| commodore_ami      | kick39106.A4000                        |
| commodore_ami      | kick40068.A4000                        |
| commodore_ami      | kick34005.CDTV                         |
| commodore_ami      | kick40060.CD32                         |
| commodore_ami      | kick40060.CD32.ext                     |
| commodore_ami      | kick40060.CD32.ext                     |
| microsoft_msx      | Machines/Shared Roms/MSX.ROM           |
| microsoft_msx      | Machines/Shared Roms/MSX2.ROM          |
| microsoft_msx      | Machines/Shared Roms/MSX2EXT.ROM       |
| microsoft_msx      | Machines/Shared Roms/MSX2P.ROM         |
| microsoft_msx      | Machines/Shared Roms/MSX2PEXT.ROM      |
| microsoft_msx      | Machines/Shared Roms/FMPAC.ROM         |
| microsoft_msx      | Machines/Shared Roms/KANJI.ROM         |
| nec_pcecd          | gexpress.pce                           |
| nec_pcecd          | syscard1.pce                           |
| nec_pcecd          | syscard2.pce                           |
| nec_pcecd          | syscard3.pce                           |
| nintendo_ds        | melonDS DS/bios7.bin                   |
| nintendo_ds        | melonDS DS/bios9.bin                   |
| nintendo_ds        | melonDS DS/dsi_bios7.bin               |
| nintendo_ds        | melonDS DS/dsi_bios9.bin               |
| nintendo_ds        | melonDS DS/dsi_firmware.bin            |
| nintendo_ds        | melonDS DS/dsi_nand.bin                |
| nintendo_ds        | melonDS DS/firmware.bin                |
| panasonic_3do      | panafz10.bin                           |
| philips_cdi        | same_cdi/bios/cdibios.zip              |
| philips_cdi        | same_cdi/bios/cdimono1.zip             |
| philips_cdi        | same_cdi/bios/cdimono2.zip             |
| sega_dc            | dc/airlbios.zip                        |
| sega_dc            | dc/awbios.zip                          |
| sega_dc            | dc/dc_boot.bin                         |
| sega_dc            | dc/f355.zip                            |
| sega_dc            | dc/f355bios.zip                        |
| sega_dc            | dc/f355dlx.zip                         |
| sega_dc            | dc/hod2bios.zip                        |
| sega_dc            | dc/naomi.zip                           |
| sega_dc            | dc/naomi2.zip                          |
| sega_dc            | dc/segasp.zip                          |
| sega_cd            | bios_CD_E.bin                          |
| sega_cd            | bios_CD_J.bin                          |
| sega_cd            | bios_CD_U.bin                          |
| sega_st            | sega_101.bin                           |
| sega_st            | mpr-17933.bin                          |
| snk_ng             | fbneo/neogeo.zip                       |
| snk_ngcd           | neocd/neocd_z.rom                      |
| sony_psx           | scph5500.bin                           |
| sony_psx           | scph5501.bin                           |
| sony_psx           | scph5502.bin                           |
| scummvm            | scummvm/extra/CM32L_CONTROL.ROM        |
| scummvm            | scummvm/extra/CM32L_PCM.ROM            |
| scummvm            | scummvm/extra/MT32_CONTROL.ROM         |
| scummvm            | scummvm/extra/MT32_PCM.ROM             |
| scummvm            | scummvm/extra/Roland_SC-55.sf2         |
| ibm_pc             | scummvm/extra/CM32L_CONTROL.ROM        |
| ibm_pc             | scummvm/extra/CM32L_PCM.ROM            |
| ibm_pc             | scummvm/extra/MT32_CONTROL.ROM         |
| ibm_pc             | scummvm/extra/MT32_PCM.ROM             |
| ibm_pc             | scummvm/extra/Roland_SC-55.sf2         |
| sharp_x68k         | keropi/cgrom.dat                       |
| sharp_x68k         | keropi/iplrom.dat                      |
| sharp_x68k         | keropi/iplrom30.dat                    |
| sharp_x68k         | keropi/iplromco.dat                    |
| sharp_x68k         | keropi/iplromxv.dat                    |

## Full BIOS File Structure

Here you can see a the full BIOS folder structure:

```sh
├── 5200.rom
├── 7800 BIOS (U).rom
├── bios_CD_E.bin
├── bios_CD_J.bin
├── bios_CD_U.bin
├── bios_E.sms
├── bios.gg
├── bios_j.sms
├── bios_MD.bin
├── bios.sms
├── bios_U.sms
├── BS-X.bin
├── capsimg.so
├── dc
│   ├── airlbios.zip
│   ├── awbios.zip
│   ├── data
│   ├── dc_boot.bin
│   ├── f355bios.zip
│   ├── f355dlx.zip
│   ├── f355.zip
│   ├── hod2bios.zip
│   ├── naomi2.zip
│   ├── naomi.zip
│   └── segasp.zip
├── disksys.rom
├── DOSBoxPureMidiCache.txt
├── fbneo
│   ├── 000-lo.lo
│   ├── bubsys.zip
│   ├── cchip.zip
│   ├── coleco.zip
│   ├── decocass.zip
│   ├── front-sp1.bin
│   ├── hiscore.dat
│   ├── isgsm.zip
│   ├── m68705p5.zip
│   ├── midssio.zip
│   ├── msx.zip
│   ├── namcoc69.zip
│   ├── namcoc70.zip
│   ├── namcoc75.zip
│   ├── neocdz.zip
│   ├── neogeo.zip
│   ├── nmk004.zip
│   ├── pgm.zip
│   ├── phoenix.key
│   ├── samples
│   │   ├── 005.zip
│   │   ├── 3bagflvt.zip
│   │   ├── armora.zip
│   │   ├── astrob.zip
│   │   ├── astrof.zip
│   │   ├── barrier.zip
│   │   ├── battles.zip
│   │   ├── berzerk.zip
│   │   ├── blockade.zip
│   │   ├── boothill.zip
│   │   ├── bosco.zip
│   │   ├── bowl3d.zip
│   │   ├── boxingb.zip
│   │   ├── brdrline.zip
│   │   ├── buckrog.zip
│   │   ├── carnival.zip
│   │   ├── circus.zip
│   │   ├── clowns.zip
│   │   ├── congo.zip
│   │   ├── cosmica.zip
│   │   ├── cosmicg.zip
│   │   ├── crash.zip
│   │   ├── dai3wksi.zip
│   │   ├── depthch.zip
│   │   ├── dkongjr.zip
│   │   ├── dkong.zip
│   │   ├── elim2.zip
│   │   ├── equites.zip
│   │   ├── fantasy.zip
│   │   ├── frogs.zip
│   │   ├── ftaerobi.zip
│   │   ├── galaga.zip
│   │   ├── gaplus.zip
│   │   ├── genpin.zip
│   │   ├── gmissile.zip
│   │   ├── gorf.zip
│   │   ├── gridlee.zip
│   │   ├── gunfight.zip
│   │   ├── homerun.zip
│   │   ├── invaders.zip
│   │   ├── invinco.zip
│   │   ├── ipminvad.zip
│   │   ├── journey.zip
│   │   ├── lrescue.zip
│   │   ├── lupin3.zip
│   │   ├── m4.zip
│   │   ├── mario.zip
│   │   ├── MM1_keyboard.zip
│   │   ├── mmagic.zip
│   │   ├── moepro88.zip
│   │   ├── moepro90.zip
│   │   ├── moepro.zip
│   │   ├── monsterb.zip
│   │   ├── mpsaikyo.zip
│   │   ├── mptennis.zip
│   │   ├── natodef.zip
│   │   ├── nsub.zip
│   │   ├── panic.zip
│   │   ├── phantom2.zip
│   │   ├── polepos.zip
│   │   ├── ptrmj.zip
│   │   ├── pulsar.zip
│   │   ├── qbert.zip
│   │   ├── rallyx.zip
│   │   ├── reactor.zip
│   │   ├── relay.zip
│   │   ├── ripcord.zip
│   │   ├── ripoff.zip
│   │   ├── robotbwl.zip
│   │   ├── safarir.zip
│   │   ├── sasuke.zip
│   │   ├── seawolf.zip
│   │   ├── sharkatt.zip
│   │   ├── smoepro.zip
│   │   ├── solarq.zip
│   │   ├── spacefb.zip
│   │   ├── spaceod.zip
│   │   ├── spacewar.zip
│   │   ├── spacfury.zip
│   │   ├── speedfrk.zip
│   │   ├── starcas.zip
│   │   ├── starcrus.zip
│   │   ├── starfire.zip
│   │   ├── starhawk.zip
│   │   ├── startrek.zip
│   │   ├── subroc3d.zip
│   │   ├── sundance.zip
│   │   ├── tacscan.zip
│   │   ├── tailg.zip
│   │   ├── tankbatt.zip
│   │   ├── targ.zip
│   │   ├── tattack.zip
│   │   ├── terao.zip
│   │   ├── thehand.zip
│   │   ├── thief.zip
│   │   ├── tranqgun.zip
│   │   ├── triplhnt.zip
│   │   ├── turbo.zip
│   │   ├── twotiger.zip
│   │   ├── vanguard.zip
│   │   ├── warrior.zip
│   │   ├── wotw.zip
│   │   ├── wow.zip
│   │   ├── xevios.zip
│   │   ├── xevious.zip
│   │   ├── zaxxon.zip
│   │   └── zektor.zip
│   ├── skns.zip
│   ├── top-sp1.bin
│   └── ym2608.zip
├── gba_bios.bin
├── gb_bios.bin
├── gbc_bios.bin
├── gexpress.pce
├── hatari
│   └── tos
│       └── tos.img
├── keropi
│   ├── cgrom.dat
│   ├── iplrom30.dat
│   ├── iplromco.dat
│   ├── iplrom.dat
│   └── iplromxv.dat
├── kick33180.A500
├── kick34005.A500
├── kick34005.CDTV
├── kick37175.A500
├── kick37350.A600
├── kick39106.A1200
├── kick39106.A4000
├── kick40060.CD32
├── kick40060.CD32.ext
├── kick40063.A600
├── kick40068.A1200
├── kick40068.A4000
├── lynxboot.img
├── Machines
│   ├── COL - ColecoVision
│   │   ├── coleco.rom
│   │   └── config.ini
│   ├── COL - ColecoVision with Opcode Memory Extension
│   │   ├── coleco.rom
│   │   └── config.ini
│   ├── COL - Spectravideo SVI-603 Coleco
│   │   ├── config.ini
│   │   └── SVI603.ROM
│   ├── MSX
│   │   └── config.ini
│   ├── MSX - Arabic
│   │   └── config.ini
│   ├── MSX - Brazilian
│   │   └── config.ini
│   ├── MSX - Canon V-20
│   │   └── config.ini
│   ├── MSX - C-BIOS
│   │   ├── cbios_main_msx1.rom
│   │   └── config.ini
│   ├── MSX - Daewoo DPC-100
│   │   └── config.ini
│   ├── MSX - Daewoo DPC-180
│   │   └── config.ini
│   ├── MSX - Daewoo DPC-200
│   │   └── config.ini
│   ├── MSX - French
│   │   └── config.ini
│   ├── MSX - German
│   │   └── config.ini
│   ├── MSX - Goldstar FC-200
│   │   └── config.ini
│   ├── MSX - Gradiente Expert 1.0
│   │   └── config.ini
│   ├── MSX - Gradiente Expert 1.1
│   │   └── config.ini
│   ├── MSX - Gradiente Expert DDPlus
│   │   └── config.ini
│   ├── MSX - Gradiente Expert Plus
│   │   └── config.ini
│   ├── MSX - Japanese
│   │   └── config.ini
│   ├── MSX - JVC HC-7GB
│   │   └── config.ini
│   ├── MSX - Korean
│   │   └── config.ini
│   ├── MSX - Mitsubishi ML-F80
│   │   └── config.ini
│   ├── MSX - Mitsubishi ML-FX1
│   │   └── config.ini
│   ├── MSX - National CF-1200
│   │   └── config.ini
│   ├── MSX - National CF-2000
│   │   └── config.ini
│   ├── MSX - National CF-2700
│   │   └── config.ini
│   ├── MSX - National CF-3000
│   │   └── config.ini
│   ├── MSX - National CF-3300
│   │   └── config.ini
│   ├── MSX - National FS-1300
│   │   └── config.ini
│   ├── MSX - National FS-4000
│   │   └── config.ini
│   ├── MSX - Philips NMS-801
│   │   └── config.ini
│   ├── MSX - Philips VG-8020
│   │   └── config.ini
│   ├── MSX - Russian
│   │   └── config.ini
│   ├── MSX - Sanyo MPC-100
│   │   └── config.ini
│   ├── MSX - Sharp Epcom HotBit 1.1
│   │   └── config.ini
│   ├── MSX - Sharp Epcom HotBit 1.2
│   │   └── config.ini
│   ├── MSX - Sony HB-201
│   │   └── config.ini
│   ├── MSX - Sony HB-201P
│   │   └── config.ini
│   ├── MSX - Sony HB-501P
│   │   └── config.ini
│   ├── MSX - Sony HB-75D
│   │   └── config.ini
│   ├── MSX - Sony HB-75P
│   │   └── config.ini
│   ├── MSX - Spanish
│   │   └── config.ini
│   ├── MSX - Spectravideo SVI-728
│   │   └── config.ini
│   ├── MSX - Spectravideo SVI-738
│   │   └── config.ini
│   ├── MSX - Spectravideo SVI-738 Henrik Gilvad
│   │   └── config.ini
│   ├── MSX - Spectravideo SVI-738 Swedish
│   │   └── config.ini
│   ├── MSX - Swedish
│   │   └── config.ini
│   ├── MSX - Talent DPC-200
│   │   └── config.ini
│   ├── MSX - Toshiba HX-10
│   │   └── config.ini
│   ├── MSX - Toshiba HX-20
│   │   └── config.ini
│   ├── MSX - Yamaha CX5M
│   │   └── config.ini
│   ├── MSX - Yamaha CX5M-128
│   │   └── config.ini
│   ├── MSX2
│   │   └── config.ini
│   ├── MSX2+
│   │   └── config.ini
│   ├── MSX2 - Arabic
│   │   └── config.ini
│   ├── MSX2+ - Brazilian
│   │   └── config.ini
│   ├── MSX2 - Brazilian
│   │   └── config.ini
│   ├── MSX2+ - C-BIOS
│   │   ├── cbios_main_msx2+.rom
│   │   ├── cbios_music.rom
│   │   ├── cbios_sub.rom
│   │   └── config.ini
│   ├── MSX2 - C-BIOS
│   │   ├── cbios_main_msx2.rom
│   │   ├── cbios_sub.rom
│   │   └── config.ini
│   ├── MSX2+ - Ciel Expert 3
│   │   └── config.ini
│   ├── MSX2 - Daewoo CPC-300
│   │   └── config.ini
│   ├── MSX2 - Daewoo CPC-400
│   │   └── config.ini
│   ├── MSX2 - Daewoo CPC-400S
│   │   └── config.ini
│   ├── MSX2+ - European
│   │   └── config.ini
│   ├── MSX2 - French
│   │   └── config.ini
│   ├── MSX2 - German
│   │   └── config.ini
│   ├── MSX2 - Gradiente Expert 2.0
│   │   └── config.ini
│   ├── MSX2 - Japanese
│   │   └── config.ini
│   ├── MSX2 - Korean
│   │   └── config.ini
│   ├── MSX2 - National FS-4500
│   │   └── config.ini
│   ├── MSX2 - National FS-4600
│   │   └── config.ini
│   ├── MSX2 - National FS-4700
│   │   └── config.ini
│   ├── MSX2 - National FS-5000
│   │   └── config.ini
│   ├── MSX2 - National FS-5500
│   │   └── config.ini
│   ├── MSX2 - Only PSG
│   │   └── config.ini
│   ├── MSX2 - Panasonic FS-A1
│   │   └── config.ini
│   ├── MSX2 - Panasonic FS-A1 MK2
│   │   └── config.ini
│   ├── MSX2 - Panasonic FS-A1F
│   │   └── config.ini
│   ├── MSX2 - Panasonic FS-A1FM
│   │   └── config.ini
│   ├── MSX2+ - Panasonic FS-A1FX
│   │   └── config.ini
│   ├── MSX2+ - Panasonic FS-A1WSX
│   │   └── config.ini
│   ├── MSX2+ - Panasonic FS-A1WX
│   │   └── config.ini
│   ├── MSX2 - Philips NMS-8220
│   │   └── config.ini
│   ├── MSX2 - Philips NMS-8245
│   │   └── config.ini
│   ├── MSX2 - Philips NMS-8250
│   │   └── config.ini
│   ├── MSX2 - Philips NMS-8255
│   │   └── config.ini
│   ├── MSX2 - Philips NMS-8280
│   │   └── config.ini
│   ├── MSX2 - Philips VG-8235
│   │   └── config.ini
│   ├── MSX2 - Philips VG-8240
│   │   └── config.ini
│   ├── MSX2 - Russian
│   │   └── config.ini
│   ├── MSX2 - Sanyo Wavy PHC-23
│   │   └── config.ini
│   ├── MSX2+ - Sanyo Wavy PHC-35J
│   │   └── config.ini
│   ├── MSX2+ - Sanyo Wavy PHC-70FD1
│   │   └── config.ini
│   ├── MSX2+ - Sanyo Wavy PHC-70FD2
│   │   └── config.ini
│   ├── MSX2 - Sharp Epcom HotBit 2.0
│   │   └── config.ini
│   ├── MSX2 - Sony HB-F1
│   │   └── config.ini
│   ├── MSX2 - Sony HB-F1II
│   │   └── config.ini
│   ├── MSX2 - Sony HB-F1XD
│   │   └── config.ini
│   ├── MSX2+ - Sony HB-F1XDJ
│   │   └── config.ini
│   ├── MSX2 - Sony HB-F1XDMK2
│   │   └── config.ini
│   ├── MSX2+ - Sony HB-F1XV
│   │   └── config.ini
│   ├── MSX2 - Sony HB-F500
│   │   └── config.ini
│   ├── MSX2 - Sony HB-F500P
│   │   └── config.ini
│   ├── MSX2 - Sony HB-F700D
│   │   └── config.ini
│   ├── MSX2 - Sony HB-F700P
│   │   └── config.ini
│   ├── MSX2 - Sony HB-F900
│   │   └── config.ini
│   ├── MSX2 - Sony HB-F9P
│   │   └── config.ini
│   ├── MSX2 - Sony HB-G900P
│   │   └── config.ini
│   ├── MSX2 - Spanish
│   │   └── config.ini
│   ├── MSX2 - Swedish
│   │   └── config.ini
│   ├── MSX2 - Talent TPC-310
│   │   └── config.ini
│   ├── MSX2 - Yamaha CX7M-128
│   │   └── config.ini
│   ├── MSXturboR
│   │   └── config.ini
│   ├── SEGA - SC-3000
│   │   └── config.ini
│   ├── SEGA - SF-7000
│   │   ├── config.ini
│   │   └── sf7000.rom
│   ├── SEGA - SG-1000
│   │   └── config.ini
│   ├── Shared Roms
│   │   ├── ARAB1.ROM
│   │   ├── ARABIC.ROM
│   │   ├── BEERIDE.ROM
│   │   ├── FMPAC.ROM
│   │   ├── GCVMX80.ROM
│   │   ├── HANGUL.ROM
│   │   ├── KANJI.ROM
│   │   ├── MICROSOLDISK.ROM
│   │   ├── MOONSOUND.ROM
│   │   ├── MSX2AREXT.ROM
│   │   ├── MSX2AR.ROM
│   │   ├── MSX2BREXT.ROM
│   │   ├── MSX2BR.ROM
│   │   ├── MSX2EXT.ROM
│   │   ├── MSX2FREXT.ROM
│   │   ├── MSX2FR.ROM
│   │   ├── MSX2GEXT.ROM
│   │   ├── MSX2G.ROM
│   │   ├── MSX2HAN.ROM
│   │   ├── MSX2JEXT.ROM
│   │   ├── MSX2J.ROM
│   │   ├── MSX2KREXT.ROM
│   │   ├── MSX2KR.ROM
│   │   ├── MSX2PEXT.ROM
│   │   ├── MSX2PMUS.ROM
│   │   ├── MSX2P.ROM
│   │   ├── MSX2REXT.ROM
│   │   ├── MSX2.ROM
│   │   ├── MSX2R.ROM
│   │   ├── MSX2SE.ROM
│   │   ├── MSX2SPEXT.ROM
│   │   ├── MSX2SP.ROM
│   │   ├── MSXAR.ROM
│   │   ├── MSXBR.ROM
│   │   ├── MSXDOS23.ROM
│   │   ├── MSXFR.ROM
│   │   ├── MSXG.ROM
│   │   ├── MSXHAN.ROM
│   │   ├── MSXJ.ROM
│   │   ├── MSXKANJI.ROM
│   │   ├── MSXKR.ROM
│   │   ├── MSX.ROM
│   │   ├── MSXR.ROM
│   │   ├── MSXSE.ROM
│   │   ├── MSXSP.ROM
│   │   ├── MSXTREXT.ROM
│   │   ├── MSXTRMUS.ROM
│   │   ├── MSXTROPT.ROM
│   │   ├── MSXTR.ROM
│   │   ├── NATIONALDISK.ROM
│   │   ├── NOVAXIS.ROM
│   │   ├── PAINT.ROM
│   │   ├── PANASONICDISK.ROM
│   │   ├── PHILIPSDISK.ROM
│   │   ├── RS232.ROM
│   │   ├── SCCPLUS.ROM
│   │   ├── SCC.ROM
│   │   ├── SHARED.TXT
│   │   ├── SUNRISEIDE.ROM
│   │   ├── SWP.ROM
│   │   └── XBASIC2.ROM
│   ├── SVI - Spectravideo SVI-318
│   │   ├── config.ini
│   │   └── svi318.rom
│   ├── SVI - Spectravideo SVI-328
│   │   ├── config.ini
│   │   └── svi328.rom
│   ├── SVI - Spectravideo SVI-328 80 Column
│   │   ├── config.ini
│   │   ├── svi328a.rom
│   │   └── svi806.rom
│   ├── SVI - Spectravideo SVI-328 80 Swedish
│   │   ├── config.ini
│   │   ├── svi328a.rom
│   │   └── svi806se.rom
│   ├── SVI - Spectravideo SVI-328 MK2
│   │   ├── config.ini
│   │   ├── svi328a.rom
│   │   └── svi806.rom
│   ├── Turbo-R
│   │   └── config.ini
│   ├── Turbo-R - European
│   │   └── config.ini
│   ├── Turbo-R - Panasonic FS-A1GT
│   │   └── config.ini
│   └── Turbo-R - Panasonic FS-A1ST
│       └── config.ini
├── mame
│   ├── cheat.7z
│   ├── hiscore
│   ├── ini
│   │   ├── plugin.ini
│   │   └── ui.ini
│   ├── plugins
│   │   ├── boot.lua
│   │   └── hiscore
│   │       ├── hiscore.dat
│   │       ├── init.lua
│   │       ├── plugin.json
│   │       └── sort_hiscore.lua
│   └── samples
│       ├── 005.zip
│       ├── 3bagfull.zip
│       ├── astrof.zip
│       ├── battles.zip
│       ├── bbc.zip
│       ├── blockade.zip
│       ├── bowl3d.zip
│       ├── buckrog.zip
│       ├── carnival.zip
│       ├── circus.zip
│       ├── clowns.zip
│       ├── congo.zip
│       ├── cosmica.zip
│       ├── cosmicg.zip
│       ├── crash.zip
│       ├── dai3wksi.zip
│       ├── depthch.zip
│       ├── equites.zip
│       ├── fantasy.zip
│       ├── fruitsamples.zip
│       ├── ftaerobi.zip
│       ├── gaplus.zip
│       ├── genpin.zip
│       ├── gmissile.zip
│       ├── gridlee.zip
│       ├── homerun.zip
│       ├── ifslots.zip
│       ├── invaders.zip
│       ├── invinco.zip
│       ├── ipminvad.zip
│       ├── journey.zip
│       ├── kst25.zip
│       ├── ktmnt2.zip
│       ├── ktopgun2.zip
│       ├── lrescue.zip
│       ├── lupin3.zip
│       ├── m4.zip
│       ├── mmagic.zip
│       ├── moepro88.zip
│       ├── moepro90.zip
│       ├── moepro.zip
│       ├── monsterb.zip
│       ├── mpsaikyo.zip
│       ├── mptennis.zip
│       ├── natodef.zip
│       ├── nsub.zip
│       ├── ozmawars.zip
│       ├── panic.zip
│       ├── phantom2.zip
│       ├── ptrmj.zip
│       ├── pulsar.zip
│       ├── qbert.zip
│       ├── rallyx.zip
│       ├── redclash.zip
│       ├── relay.zip
│       ├── ripcord.zip
│       ├── robotbwl.zip
│       ├── safarir.zip
│       ├── sasuke.zip
│       ├── seawolf.zip
│       ├── sharkatt.zip
│       ├── smoepro.zip
│       ├── spacefb.zip
│       ├── spaceod.zip
│       ├── subroc3d.zip
│       ├── targ.zip
│       ├── tattack.zip
│       ├── terao.zip
│       ├── thehand.zip
│       ├── thief.zip
│       ├── triplhnt.zip
│       ├── turbo.zip
│       ├── twotiger.zip
│       ├── vanguard.zip
│       ├── zaxxon.zip
│       └── zerohour.zip
├── mame2003-plus
│   ├── artwork
│   ├── hiscore.dat
│   └── samples
│       ├── 005.zip
│       ├── 3bagfull.zip
│       ├── astrof.zip
│       ├── battles.zip
│       ├── bbc.zip
│       ├── blockade.zip
│       ├── bowl3d.zip
│       ├── buckrog.zip
│       ├── carnival.zip
│       ├── circus.zip
│       ├── clowns.zip
│       ├── congo.zip
│       ├── cosmica.zip
│       ├── cosmicg.zip
│       ├── crash.zip
│       ├── dai3wksi.zip
│       ├── depthch.zip
│       ├── equites.zip
│       ├── fantasy.zip
│       ├── fruitsamples.zip
│       ├── ftaerobi.zip
│       ├── gaplus.zip
│       ├── genpin.zip
│       ├── gmissile.zip
│       ├── gridlee.zip
│       ├── homerun.zip
│       ├── ifslots.zip
│       ├── invaders.zip
│       ├── invinco.zip
│       ├── ipminvad.zip
│       ├── journey.zip
│       ├── kst25.zip
│       ├── ktmnt2.zip
│       ├── ktopgun2.zip
│       ├── lrescue.zip
│       ├── lupin3.zip
│       ├── m4.zip
│       ├── mmagic.zip
│       ├── moepro88.zip
│       ├── moepro90.zip
│       ├── moepro.zip
│       ├── monsterb.zip
│       ├── mpsaikyo.zip
│       ├── mptennis.zip
│       ├── natodef.zip
│       ├── nsub.zip
│       ├── ozmawars.zip
│       ├── panic.zip
│       ├── phantom2.zip
│       ├── ptrmj.zip
│       ├── pulsar.zip
│       ├── qbert.zip
│       ├── rallyx.zip
│       ├── redclash.zip
│       ├── relay.zip
│       ├── ripcord.zip
│       ├── robotbwl.zip
│       ├── safarir.zip
│       ├── sasuke.zip
│       ├── seawolf.zip
│       ├── sharkatt.zip
│       ├── smoepro.zip
│       ├── spacefb.zip
│       ├── spaceod.zip
│       ├── subroc3d.zip
│       ├── targ.zip
│       ├── tattack.zip
│       ├── terao.zip
│       ├── thehand.zip
│       ├── thief.zip
│       ├── triplhnt.zip
│       ├── turbo.zip
│       ├── twotiger.zip
│       ├── vanguard.zip
│       ├── zaxxon.zip
│       └── zerohour.zip
├── melonDS DS
│   ├── bios7.bin
│   ├── bios9.bin
│   ├── dsi_bios7.bin
│   ├── dsi_bios9.bin
│   ├── dsi_firmware.bin
│   ├── dsi_nand.bin
│   └── firmware.bin
├── mpr-17933.bin
├── neocd
│   ├── neocd.srm
│   ├── neocd_z.rom
│   └── uni-bioscd.rom
├── panafz10.bin
├── same_cdi
│   └── bios
│       ├── cdibios.zip
│       ├── cdimono1.zip
│       └── cdimono2.zip
├── scph5500.bin
├── scph5501.bin
├── scph5502.bin
├── scummvm
│   ├── extra
│   │   ├── access.dat
│   │   ├── achievements.dat
│   │   ├── classicmacfonts.dat
│   │   ├── CM32L_CONTROL.ROM
│   │   ├── CM32L_PCM.ROM
│   │   ├── create-playground3d-data.sh
│   │   ├── create-testbed-data.sh
│   │   ├── cryo.dat
│   │   ├── cryomni3d.dat
│   │   ├── drascula.dat
│   │   ├── encoding.dat
│   │   ├── fonts-cjk.dat
│   │   ├── fonts.dat
│   │   ├── freescape.dat
│   │   ├── grim-patch.lab
│   │   ├── hadesch_translations.dat
│   │   ├── hugo.dat
│   │   ├── kyra.dat
│   │   ├── lure.dat
│   │   ├── macgui.dat
│   │   ├── macventure.dat
│   │   ├── mm.dat
│   │   ├── monkey4-patch.m4b
│   │   ├── mort.dat
│   │   ├── MT32_CONTROL.ROM
│   │   ├── MT32_PCM.ROM
│   │   ├── myst3.dat
│   │   ├── nancy.dat
│   │   ├── neverhood.dat
│   │   ├── prince_translation.dat
│   │   ├── queen.tbl
│   │   ├── README
│   │   ├── Roland_SC-55.sf2
│   │   ├── sky.cpt
│   │   ├── supernova.dat
│   │   ├── teenagent.dat
│   │   ├── titanic.dat
│   │   ├── tony.dat
│   │   ├── toon.dat
│   │   ├── ultima8.dat
│   │   ├── ultima.dat
│   │   ├── wintermute.zip
│   │   └── xeen.ccs
│   ├── soundfonts
│   │   ├── FluidR3_GM.sf2
│   │   ├── GM_Roland.sf2
│   │   ├── Roland_SC-55.sf2
│   │   └── UHD3.sf2
│   └── theme
├── scummvm.ini
├── sega_101.bin
├── syscard1.pce
├── syscard2.pce
└── syscard3.pce
```