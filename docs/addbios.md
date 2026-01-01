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
| scummvm            | scummvm/extra/Roland_SC-55.sf2         |
| scummvm            | scummvm/extra/CM32L_CONTROL.ROM        |
| scummvm            | scummvm/extra/CM32L_PCM.ROM            |
| scummvm            | scummvm/extra/MT32_CONTROL.ROM         |
| scummvm            | scummvm/extra/MT32_PCM.ROM             |
| sharp_x68k         | keropi/cgrom.dat                       |
| sharp_x68k         | keropi/iplrom.dat                      |
| sharp_x68k         | keropi/iplrom30.dat                    |
| sharp_x68k         | keropi/iplromco.dat                    |
| sharp_x68k         | keropi/iplromxv.dat                    |

## Full BIOS File Structure

Here you can see a picture of the full BIOS folder structure:

![bios](img/bios.png)