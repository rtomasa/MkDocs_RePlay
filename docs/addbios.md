# Adding BIOS

Many systems require some mandatory BIOS files to run or use some special configurations. You can copy your BIOS files into the corresponding `/bios` folder in your storage unit.

**IMPORTANT:** RePlayOS will check for any missing BIOS files required by the system you are trying to use. If any BIOS file is missing, it will prevent you from loading games until you copy all required BIOS files.

## Minimum BIOS System Files

The following table is a reference about the minimum required BIOS files used by the different systems in RePlayOS:

**NOTE:** please check the [full BIOS folder structure](#full-bios-file-structure) in case that some system is not properly booting with the minimum bios files.

| System | BIOS / File |
|---|---|
| `arcade_dc` | `dc/airlbios.zip` |
| `arcade_dc` | `dc/awbios.zip` |
| `arcade_dc` | `dc/dc_boot.bin` |
| `arcade_dc` | `dc/f355.zip` |
| `arcade_dc` | `dc/f355bios.zip` |
| `arcade_dc` | `dc/f355dlx.zip` |
| `arcade_dc` | `dc/hod2bios.zip` |
| `arcade_dc` | `dc/naomi.zip` |
| `arcade_dc` | `dc/naomi2.zip` |
| `arcade_dc` | `dc/segasp.zip` |
| `arcade_triforce` | `dolphin-emu/Sys/codehandler.bin` |
| `atari_5200` | `5200.rom` |
| `atari_7800` | `7800 BIOS (U).rom` |
| `atari_lynx` | `lynxboot.img` |
| `commodore_ami` | `capsimg.so` |
| `commodore_ami` | `kick33180.A500` |
| `commodore_ami` | `kick34005.A500` |
| `commodore_ami` | `kick37175.A500` |
| `commodore_ami` | `kick37350.A600` |
| `commodore_ami` | `kick40063.A600` |
| `commodore_ami` | `kick39106.A1200` |
| `commodore_ami` | `kick40068.A1200` |
| `commodore_ami` | `kick39106.A4000` |
| `commodore_ami` | `kick40068.A4000` |
| `commodore_ami` | `kick34005.CDTV` |
| `commodore_ami` | `kick40060.CD32` |
| `commodore_ami` | `kick40060.CD32.ext` |
| `microsoft_msx` | `Machines/Shared Roms/MSX.ROM` |
| `microsoft_msx` | `Machines/Shared Roms/MSX2.ROM` |
| `microsoft_msx` | `Machines/Shared Roms/MSX2EXT.ROM` |
| `microsoft_msx` | `Machines/Shared Roms/MSX2P.ROM` |
| `microsoft_msx` | `Machines/Shared Roms/MSX2PEXT.ROM` |
| `microsoft_msx` | `Machines/Shared Roms/FMPAC.ROM` |
| `microsoft_msx` | `Machines/Shared Roms/KANJI.ROM` |
| `nec_pcecd` | `gexpress.pce` |
| `nec_pcecd` | `syscard1.pce` |
| `nec_pcecd` | `syscard2.pce` |
| `nec_pcecd` | `syscard3.pce` |
| `nintendo_gc` | `dolphin-emu/Sys/codehandler.bin` |
| `nintendo_wii` | `dolphin-emu/Sys/codehandler.bin` |
| `nintendo_ds` | `melonDS DS/bios7.bin` |
| `nintendo_ds` | `melonDS DS/bios9.bin` |
| `nintendo_ds` | `melonDS DS/dsi_bios7.bin` |
| `nintendo_ds` | `melonDS DS/dsi_bios9.bin` |
| `nintendo_ds` | `melonDS DS/dsi_firmware.bin` |
| `nintendo_ds` | `melonDS DS/dsi_nand.bin` |
| `nintendo_ds` | `melonDS DS/firmware.bin` |
| `panasonic_3do` | `panafz10.bin` |
| `philips_cdi` | `same_cdi/bios/cdibios.zip` |
| `philips_cdi` | `same_cdi/bios/cdimono1.zip` |
| `philips_cdi` | `same_cdi/bios/cdimono2.zip` |
| `sega_dc` | `dc/airlbios.zip` |
| `sega_dc` | `dc/awbios.zip` |
| `sega_dc` | `dc/dc_boot.bin` |
| `sega_dc` | `dc/f355.zip` |
| `sega_dc` | `dc/f355bios.zip` |
| `sega_dc` | `dc/f355dlx.zip` |
| `sega_dc` | `dc/hod2bios.zip` |
| `sega_dc` | `dc/naomi.zip` |
| `sega_dc` | `dc/naomi2.zip` |
| `sega_dc` | `dc/segasp.zip` |
| `sega_cd` | `bios_CD_E.bin` |
| `sega_cd` | `bios_CD_J.bin` |
| `sega_cd` | `bios_CD_U.bin` |
| `sega_st` | `sega_101.bin` |
| `sega_st` | `mpr-17933.bin` |
| `snk_ng` | `fbneo/neogeo.zip` |
| `snk_ngcd` | `neocd/neocd_z.rom` |
| `sony_psx` | `scph5500.bin` |
| `sony_psx` | `scph5501.bin` |
| `sony_psx` | `scph5502.bin` |
| `sony_ps2` | `pcsx2/bios/SCPH-70004_BIOS_V12_PAL_200.BIN` |
| `sony_ps2` | `pcsx2/bios/SCPH-70004_BIOS_V12_PAL_200.EROM` |
| `sony_ps2` | `pcsx2/bios/SCPH-70004_BIOS_V12_PAL_200.MEC` |
| `sony_ps2` | `pcsx2/bios/SCPH-70004_BIOS_V12_PAL_200.NVM` |
| `sony_ps2` | `pcsx2/bios/SCPH-70004_BIOS_V12_PAL_200.ROM1` |
| `sony_ps2` | `pcsx2/bios/SCPH-70004_BIOS_V12_PAL_200.ROM2` |
| `sony_ps2` | `pcsx2/bios/SCPH-70012_BIOS_V12_USA_200.bin` |
| `sony_ps2` | `pcsx2/bios/SCPH-70012_BIOS_V12_USA_200.MEC` |
| `sony_ps2` | `pcsx2/bios/SCPH-70012_BIOS_V12_USA_200.NVM` |
| `sony_psp` | `PPSSPP/compat.ini` |
| `sony_psp` | `PPSSPP/lang/en_US.ini` |
| `sony_psp` | `PPSSPP/ppge_atlas.meta` |
| `sony_psp` | `PPSSPP/ppge_atlas.zim` |
| `sony_psp` | `PPSSPP/vfpu/vfpu_sin_lut_delta.dat` |
| `sony_psp` | `PPSSPP/vfpu/vfpu_sin_lut_exceptions.dat` |
| `sony_psp` | `PPSSPP/vfpu/vfpu_sin_lut8192.dat` |
| `sony_psp` | `PPSSPP/vfpu/vfpu_sin_lut_interval_delta.dat` |
| `scummvm` | `scummvm/extra/CM32L_CONTROL.ROM` |
| `scummvm` | `scummvm/extra/CM32L_PCM.ROM` |
| `scummvm` | `scummvm/extra/MT32_CONTROL.ROM` |
| `scummvm` | `scummvm/extra/MT32_PCM.ROM` |
| `scummvm` | `scummvm/extra/Roland_SC-55.sf2` |
| `ibm_pc` | `scummvm/extra/CM32L_CONTROL.ROM` |
| `ibm_pc` | `scummvm/extra/CM32L_PCM.ROM` |
| `ibm_pc` | `scummvm/extra/MT32_CONTROL.ROM` |
| `ibm_pc` | `scummvm/extra/MT32_PCM.ROM` |
| `ibm_pc` | `scummvm/extra/Roland_SC-55.sf2` |
| `sharp_x68k` | `keropi/cgrom.dat` |
| `sharp_x68k` | `keropi/iplrom.dat` |
| `sharp_x68k` | `keropi/iplrom30.dat` |
| `sharp_x68k` | `keropi/iplromco.dat` |
| `sharp_x68k` | `keropi/iplromxv.dat` |
| `sinclair_zx` | `fuse/128p-0.rom` |
| `sinclair_zx` | `fuse/128p-1.rom` |
| `sinclair_zx` | `fuse/256s-0.rom` |
| `sinclair_zx` | `fuse/256s-1.rom` |
| `sinclair_zx` | `fuse/256s-2.rom` |
| `sinclair_zx` | `fuse/256s-3.rom` |
| `sinclair_zx` | `fuse/gluck.rom` |
| `sinclair_zx` | `fuse/trdos.rom` |

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
├── dolphin-emu
│   └── Sys
│       ├── ApprovedInis.json
│       ├── codehandler.bin
│       ├── GameSettings
│       │   ├── 0000000100000002.ini
│       │   ├── C.ini
│       │   ├── D43E01.ini
│       │   ├── D43.ini
│       │   ├── D43J01.ini
│       │   ├── D44.ini
│       │   ├── D56E01.ini
│       │   ├── D85.ini
│       │   ├── D86.ini
│       │   ├── D93U01.ini
│       │   ├── D95.ini
│       │   ├── DAX.ini
│       │   ├── DD2.ini
│       │   ├── DJU.ini
│       │   ├── DLS.ini
│       │   ├── DPOJ8P.ini
│       │   ├── DPSJ8P.ini
│       │   ├── DQA.ini
│       │   ├── DSR.ini
│       │   ├── E52.ini
│       │   ├── E53.ini
│       │   ├── E54.ini
│       │   ├── E55.ini
│       │   ├── E56.ini
│       │   ├── E57.ini
│       │   ├── E5Z.ini
│       │   ├── E62.ini
│       │   ├── E63.ini
│       │   ├── E6N.ini
│       │   ├── E6Q.ini
│       │   ├── E6V.ini
│       │   ├── E6W.ini
│       │   ├── E6X.ini
│       │   ├── E73.ini
│       │   ├── E78.ini
│       │   ├── E79.ini
│       │   ├── E7V.ini
│       │   ├── E7Z.ini
│       │   ├── EA2.ini
│       │   ├── EA3.ini
│       │   ├── EA4.ini
│       │   ├── EA5.ini
│       │   ├── EA6.ini
│       │   ├── EA7.ini
│       │   ├── EA8.ini
│       │   ├── EA9.ini
│       │   ├── EAA.ini
│       │   ├── EAB.ini
│       │   ├── EAC.ini
│       │   ├── EAD.ini
│       │   ├── EAE.ini
│       │   ├── EAF.ini
│       │   ├── EAG.ini
│       │   ├── EAH.ini
│       │   ├── EAI.ini
│       │   ├── EAJ.ini
│       │   ├── EAK.ini
│       │   ├── EAL.ini
│       │   ├── EAM.ini
│       │   ├── EAN.ini
│       │   ├── EAO.ini
│       │   ├── EAP.ini
│       │   ├── EAQ.ini
│       │   ├── EAR.ini
│       │   ├── EAS.ini
│       │   ├── EAT.ini
│       │   ├── EAU.ini
│       │   ├── EAV.ini
│       │   ├── EAW.ini
│       │   ├── EAY.ini
│       │   ├── EAZ.ini
│       │   ├── EB2.ini
│       │   ├── EB3.ini
│       │   ├── EB4.ini
│       │   ├── EB5.ini
│       │   ├── EB6.ini
│       │   ├── EB7.ini
│       │   ├── EB8.ini
│       │   ├── EB9.ini
│       │   ├── EBA.ini
│       │   ├── EBB.ini
│       │   ├── EBC.ini
│       │   ├── EBD.ini
│       │   ├── EBE.ini
│       │   ├── EBF.ini
│       │   ├── EBG.ini
│       │   ├── EBK.ini
│       │   ├── EBL.ini
│       │   ├── EBM.ini
│       │   ├── EBN.ini
│       │   ├── EBO.ini
│       │   ├── EBP.ini
│       │   ├── EBQ.ini
│       │   ├── EBR.ini
│       │   ├── EBS.ini
│       │   ├── EBT.ini
│       │   ├── EBU.ini
│       │   ├── EBV.ini
│       │   ├── EBW.ini
│       │   ├── EBX.ini
│       │   ├── EBZ.ini
│       │   ├── ECA.ini
│       │   ├── ECC.ini
│       │   ├── ECD.ini
│       │   ├── ECE.ini
│       │   ├── ECF.ini
│       │   ├── ECG.ini
│       │   ├── ECH.ini
│       │   ├── ECI.ini
│       │   ├── ECJ.ini
│       │   ├── ECK.ini
│       │   ├── ECL.ini
│       │   ├── ECM.ini
│       │   ├── ECN.ini
│       │   ├── E.ini
│       │   ├── FAAE01.ini
│       │   ├── FABE01.ini
│       │   ├── FABP01.ini
│       │   ├── FACE01.ini
│       │   ├── FACP01.ini
│       │   ├── FAFE01.ini
│       │   ├── FAGE01.ini
│       │   ├── FAHE01.ini
│       │   ├── FAIE01.ini
│       │   ├── FAJE01.ini
│       │   ├── FAJP01.ini
│       │   ├── FAKE01.ini
│       │   ├── FAKP01.ini
│       │   ├── FALE01.ini
│       │   ├── FAME01.ini
│       │   ├── FANE01.ini
│       │   ├── FAOE01.ini
│       │   ├── FARE01.ini
│       │   ├── FASE01.ini
│       │   ├── F.ini
│       │   ├── G2BE5G.ini
│       │   ├── G2B.ini
│       │   ├── G2BP7D.ini
│       │   ├── G2C.ini
│       │   ├── G2FE78.ini
│       │   ├── G2ME01.ini
│       │   ├── G2M.ini
│       │   ├── G2MP01.ini
│       │   ├── G2O.ini
│       │   ├── G2RE52.ini
│       │   ├── G2VE08.ini
│       │   ├── G2V.ini
│       │   ├── G2VP08.ini
│       │   ├── G2X.ini
│       │   ├── G3A.ini
│       │   ├── G3F.ini
│       │   ├── G3L.ini
│       │   ├── G3Q.ini
│       │   ├── G3R.ini
│       │   ├── G3RP52.ini
│       │   ├── G3X.ini
│       │   ├── G3YP52.ini
│       │   ├── G4AEE9.ini
│       │   ├── G4C.ini
│       │   ├── G4GEE9.ini
│       │   ├── G4I.ini
│       │   ├── G4ME69.ini
│       │   ├── G4M.ini
│       │   ├── G4NJDA.ini
│       │   ├── G4P.ini
│       │   ├── G4QE01.ini
│       │   ├── G4S.ini
│       │   ├── G4SP01.ini
│       │   ├── G4Z.ini
│       │   ├── G5B.ini
│       │   ├── G5D.ini
│       │   ├── G5N.ini
│       │   ├── G5SE7D.ini
│       │   ├── G5SP7D.ini
│       │   ├── G5T.ini
│       │   ├── G6Q.ini
│       │   ├── G6S.ini
│       │   ├── G6T.ini
│       │   ├── G6W.ini
│       │   ├── G8ME01.ini
│       │   ├── G8M.ini
│       │   ├── G8MJ01.ini
│       │   ├── G8MP01.ini
│       │   ├── G8W.ini
│       │   ├── G8WP01.ini
│       │   ├── G95.ini
│       │   ├── G96.ini
│       │   ├── G97.ini
│       │   ├── G99.ini
│       │   ├── G9R.ini
│       │   ├── G9SE8P.ini
│       │   ├── G9S.ini
│       │   ├── G9SJ8P.ini
│       │   ├── G9SP8P.ini
│       │   ├── G9T.ini
│       │   ├── GAA.ini
│       │   ├── GAFE01.ini
│       │   ├── GAF.ini
│       │   ├── GAHEGG.ini
│       │   ├── GAK.ini
│       │   ├── GALE01r0.ini
│       │   ├── GALE01r1.ini
│       │   ├── GALE01r2.ini
│       │   ├── GAL.ini
│       │   ├── GALP01.ini
│       │   ├── GAP.ini
│       │   ├── GAS.ini
│       │   ├── GAUE08.ini
│       │   ├── GAU.ini
│       │   ├── GAV.ini
│       │   ├── GAY.ini
│       │   ├── GAZE69.ini
│       │   ├── GB3.ini
│       │   ├── GB4E51.ini
│       │   ├── GBHEC8.ini
│       │   ├── GBH.ini
│       │   ├── GBLE52.ini
│       │   ├── GBL.ini
│       │   ├── GBLP52.ini
│       │   ├── GBM.ini
│       │   ├── GBOP51.ini
│       │   ├── GBRJ18.ini
│       │   ├── GBSE8P.ini
│       │   ├── GBS.ini
│       │   ├── GBSP8P.ini
│       │   ├── GBV.ini
│       │   ├── GBW.ini
│       │   ├── GBZ.ini
│       │   ├── GBZP08.ini
│       │   ├── GC2.ini
│       │   ├── GC3.ini
│       │   ├── GC6E01.ini
│       │   ├── GC6.ini
│       │   ├── GC6J01.ini
│       │   ├── GC6P01.ini
│       │   ├── GC8JA4.ini
│       │   ├── GC9.ini
│       │   ├── GCA.ini
│       │   ├── GCBE7D.ini
│       │   ├── GCBP7D.ini
│       │   ├── GCCE01.ini
│       │   ├── GCC.ini
│       │   ├── GCCJGC.ini
│       │   ├── GCCP01.ini
│       │   ├── GCD.ini
│       │   ├── GCDP08.ini
│       │   ├── GCE.ini
│       │   ├── GCH.ini
│       │   ├── GCI.ini
│       │   ├── GCN.ini
│       │   ├── GCO.ini
│       │   ├── GCVEEB.ini
│       │   ├── GCZ.ini
│       │   ├── GD7E70.ini
│       │   ├── GD7.ini
│       │   ├── GD7PB2.ini
│       │   ├── GDDE41.ini
│       │   ├── GDD.ini
│       │   ├── GDEE71.ini
│       │   ├── GDE.ini
│       │   ├── GDG.ini
│       │   ├── GDJEB2.ini
│       │   ├── GDK.ini
│       │   ├── GDM.ini
│       │   ├── GDQ.ini
│       │   ├── GDREAF.ini
│       │   ├── GDRP69.ini
│       │   ├── GDSE78.ini
│       │   ├── GDS.ini
│       │   ├── GDSP78.ini
│       │   ├── GDTE69.ini
│       │   ├── GDT.ini
│       │   ├── GDV.ini
│       │   ├── GDX.ini
│       │   ├── GE3.ini
│       │   ├── GE4.ini
│       │   ├── GE5EA4.ini
│       │   ├── GE9.ini
│       │   ├── GEA.ini
│       │   ├── GEDE01.ini
│       │   ├── GED.ini
│       │   ├── GEDJ01.ini
│       │   ├── GEDP01.ini
│       │   ├── GEDW01.ini
│       │   ├── GEME7F.ini
│       │   ├── GEMJ28.ini
│       │   ├── GEN.ini
│       │   ├── GEO.ini
│       │   ├── GEYJ6E.ini
│       │   ├── GEYP6E.ini
│       │   ├── GEZE8P.ini
│       │   ├── GEZ.ini
│       │   ├── GEZP8P.ini
│       │   ├── GF4.ini
│       │   ├── GF7E01.ini
│       │   ├── GF7.ini
│       │   ├── GF7P01.ini
│       │   ├── GF8E69.ini
│       │   ├── GFD.ini
│       │   ├── GFEE01.ini
│       │   ├── GFEJ01.ini
│       │   ├── GFF.ini
│       │   ├── GFG.ini
│       │   ├── GFH.ini
│       │   ├── GFO.ini
│       │   ├── GFP.ini
│       │   ├── GFQEA4.ini
│       │   ├── GFTE01.ini
│       │   ├── GFW.ini
│       │   ├── GFYE69.ini
│       │   ├── GFY.ini
│       │   ├── GFZE01.ini
│       │   ├── GFZ.ini
│       │   ├── GFZJ01.ini
│       │   ├── GFZJ8P.ini
│       │   ├── GFZP01.ini
│       │   ├── GGC.ini
│       │   ├── GGE.ini
│       │   ├── GGGE6E.ini
│       │   ├── GGN.ini
│       │   ├── GGR.ini
│       │   ├── GGSEA4.ini
│       │   ├── GGS.ini
│       │   ├── GGSPA4.ini
│       │   ├── GGTE01.ini
│       │   ├── GGTJ01.ini
│       │   ├── GGTP01.ini
│       │   ├── GGVD78.ini
│       │   ├── GGVE78.ini
│       │   ├── GGV.ini
│       │   ├── GGVP78.ini
│       │   ├── GGVX78.ini
│       │   ├── GGY.ini
│       │   ├── GGZ.ini
│       │   ├── GH2E69.ini
│       │   ├── GH2P69.ini
│       │   ├── GH7.ini
│       │   ├── GH9.ini
│       │   ├── GHAE08.ini
│       │   ├── GHAE6E.ini
│       │   ├── GHAJ08.ini
│       │   ├── GHAP08.ini
│       │   ├── GHKD7D.ini
│       │   ├── GHKE7D.ini
│       │   ├── GHKF7D.ini
│       │   ├── GHK.ini
│       │   ├── GHKP7D.ini
│       │   ├── GHKS7D.ini
│       │   ├── GHLE69.ini
│       │   ├── GHME4F.ini
│       │   ├── GHN.ini
│       │   ├── GHQE7D.ini
│       │   ├── GHQP7D.ini
│       │   ├── GHRE78.ini
│       │   ├── GHR.ini
│       │   ├── GHSE69.ini
│       │   ├── GHS.ini
│       │   ├── GHSP69.ini
│       │   ├── GHV.ini
│       │   ├── GHY.ini
│       │   ├── GHZW6E.ini
│       │   ├── GIA.ini
│       │   ├── GICD78.ini
│       │   ├── GICE78.ini
│       │   ├── GICF78.ini
│       │   ├── GICH78.ini
│       │   ├── GIC.ini
│       │   ├── GICJG9.ini
│       │   ├── GICP78.ini
│       │   ├── GIGJ8P.ini
│       │   ├── GIH.ini
│       │   ├── GIHP78.ini
│       │   ├── GIL.ini
│       │   ├── GINE69.ini
│       │   ├── GIQE78.ini
│       │   ├── GIQ.ini
│       │   ├── GIQJ8P.ini
│       │   ├── GIQX78.ini
│       │   ├── GIQY78.ini
│       │   ├── GIS.ini
│       │   ├── GIT.ini
│       │   ├── GIZ.ini
│       │   ├── GJAP6E.ini
│       │   ├── GJB.ini
│       │   ├── GJCE8P.ini
│       │   ├── GJD.ini
│       │   ├── GJF.ini
│       │   ├── GJK.ini
│       │   ├── GJN.ini
│       │   ├── GJUE78.ini
│       │   ├── GJWE78.ini
│       │   ├── GJXP51.ini
│       │   ├── GJY.ini
│       │   ├── GK2E52.ini
│       │   ├── GK2.ini
│       │   ├── GK4E01.ini
│       │   ├── GK4.ini
│       │   ├── GK5.ini
│       │   ├── GK7.ini
│       │   ├── GKB.ini
│       │   ├── GKBPAF.ini
│       │   ├── GKDP01.ini
│       │   ├── GKH.ini
│       │   ├── GKL.ini
│       │   ├── GKM.ini
│       │   ├── GKNEB2.ini
│       │   ├── GKO.ini
│       │   ├── GKRPB2.ini
│       │   ├── GKS.ini
│       │   ├── GKU.ini
│       │   ├── GKWJ18.ini
│       │   ├── GKYE01.ini
│       │   ├── GKY.ini
│       │   ├── GKYJ01.ini
│       │   ├── GKYP01.ini
│       │   ├── GKZ.ini
│       │   ├── GL5.ini
│       │   ├── GL7.ini
│       │   ├── GL8.ini
│       │   ├── GLC.ini
│       │   ├── GLEE08.ini
│       │   ├── GLE.ini
│       │   ├── GLEJ08.ini
│       │   ├── GLEP08.ini
│       │   ├── GLG.ini
│       │   ├── GLKJ6E.ini
│       │   ├── GLLP6E.ini
│       │   ├── GLME01.ini
│       │   ├── GLM.ini
│       │   ├── GLMP01.ini
│       │   ├── GLNE69.ini
│       │   ├── GLR.ini
│       │   ├── GLSD64.ini
│       │   ├── GLSE64.ini
│       │   ├── GLSF64.ini
│       │   ├── GLS.ini
│       │   ├── GLSP64.ini
│       │   ├── GLZ.ini
│       │   ├── GM2.ini
│       │   ├── GM3.ini
│       │   ├── GM4E01.ini
│       │   ├── GM4.ini
│       │   ├── GM4P01.ini
│       │   ├── GM5.ini
│       │   ├── GM6.ini
│       │   ├── GM8E01.ini
│       │   ├── GM8.ini
│       │   ├── GMBE8P.ini
│       │   ├── GMB.ini
│       │   ├── GMBP8P.ini
│       │   ├── GMD.ini
│       │   ├── GMF.ini
│       │   ├── GMH.ini
│       │   ├── GMI.ini
│       │   ├── GMK.ini
│       │   ├── GMNE78.ini
│       │   ├── GMN.ini
│       │   ├── GMNP78.ini
│       │   ├── GMOP70.ini
│       │   ├── GMPE01.ini
│       │   ├── GMPJ01.ini
│       │   ├── GMPP01.ini
│       │   ├── GMSE01.ini
│       │   ├── GMS.ini
│       │   ├── GMSJ01.ini
│       │   ├── GMSJ01r0.ini
│       │   ├── GMSJ01r1.ini
│       │   ├── GMSP01.ini
│       │   ├── GMXE70.ini
│       │   ├── GMX.ini
│       │   ├── GN4.ini
│       │   ├── GN7.ini
│       │   ├── GNC.ini
│       │   ├── GNE.ini
│       │   ├── GNHE5d.ini
│       │   ├── GNI.ini
│       │   ├── GNJ.ini
│       │   ├── GNLE82.ini
│       │   ├── GNLJ82.ini
│       │   ├── GNM.ini
│       │   ├── GNN.ini
│       │   ├── GNO.ini
│       │   ├── GNWE69.ini
│       │   ├── GNW.ini
│       │   ├── GO2E4F.ini
│       │   ├── GO2.ini
│       │   ├── GO7E69.ini
│       │   ├── GO7F69.ini
│       │   ├── GO7P69.ini
│       │   ├── GOCE5D.ini
│       │   ├── GOF.ini
│       │   ├── GOME01.ini
│       │   ├── GOM.ini
│       │   ├── GOMP01.ini
│       │   ├── GONE69.ini
│       │   ├── GOQ.ini
│       │   ├── GOS.ini
│       │   ├── GOWE69.ini
│       │   ├── GOW.ini
│       │   ├── GOYE69.ini
│       │   ├── GOY.ini
│       │   ├── GP2.ini
│       │   ├── GP3.ini
│       │   ├── GP4J18.ini
│       │   ├── GP5E01.ini
│       │   ├── GP5.ini
│       │   ├── GP5J01.ini
│       │   ├── GP5P01.ini
│       │   ├── GP6E01.ini
│       │   ├── GP6.ini
│       │   ├── GP6J01.ini
│       │   ├── GP6P01.ini
│       │   ├── GP7E01.ini
│       │   ├── GP7J01.ini
│       │   ├── GP7P01.ini
│       │   ├── GPA.ini
│       │   ├── GPE.ini
│       │   ├── GPH.ini
│       │   ├── GPIE01r0.ini
│       │   ├── GPIE01r1.ini
│       │   ├── GPIP01.ini
│       │   ├── GPK.ini
│       │   ├── GPL.ini
│       │   ├── GPNE08.ini
│       │   ├── GPNP08.ini
│       │   ├── GPOE8P.ini
│       │   ├── GPOE8Pr0.ini
│       │   ├── GPOE8Pr1.ini
│       │   ├── GPO.ini
│       │   ├── GPOP8P.ini
│       │   ├── GPS.ini
│       │   ├── GPSP8P.ini
│       │   ├── GPT.ini
│       │   ├── GPVE01.ini
│       │   ├── GPVP01.ini
│       │   ├── GPXJ01.ini
│       │   ├── GQ4.ini
│       │   ├── GQC.ini
│       │   ├── GQN.ini
│       │   ├── GQPE78.ini
│       │   ├── GQP.ini
│       │   ├── GQPP78.ini
│       │   ├── GQQ.ini
│       │   ├── GQSDAF.ini
│       │   ├── GQSEAF.ini
│       │   ├── GQSFAF.ini
│       │   ├── GQS.ini
│       │   ├── GQX.ini
│       │   ├── GR2E52.ini
│       │   ├── GR2.ini
│       │   ├── GR2J52.ini
│       │   ├── GR2P52.ini
│       │   ├── GR6.ini
│       │   ├── GRA.ini
│       │   ├── GRB.ini
│       │   ├── GREE08.ini
│       │   ├── GREJ08.ini
│       │   ├── GRH.ini
│       │   ├── GRJ.ini
│       │   ├── GRK.ini
│       │   ├── GRNE52.ini
│       │   ├── GRN.ini
│       │   ├── GRNJ52.ini
│       │   ├── GRNP52.ini
│       │   ├── GROE5Z.ini
│       │   ├── GRQ.ini
│       │   ├── GRSPAF.ini
│       │   ├── GRUE78.ini
│       │   ├── GRU.ini
│       │   ├── GRYE41.ini
│       │   ├── GRY.ini
│       │   ├── GS2E78.ini
│       │   ├── GS2.ini
│       │   ├── GSAE01r0.ini
│       │   ├── GSAE01r1.ini
│       │   ├── GSAP01.ini
│       │   ├── GSB.ini
│       │   ├── GSM.ini
│       │   ├── GSNE8P.ini
│       │   ├── GSN.ini
│       │   ├── GSNJ8P.ini
│       │   ├── GSNP8P.ini
│       │   ├── GSO.ini
│       │   ├── GSPE69.ini
│       │   ├── GSPP69.ini
│       │   ├── GSQ.ini
│       │   ├── GSR.ini
│       │   ├── GSSE8P.ini
│       │   ├── GSS.ini
│       │   ├── GST.ini
│       │   ├── GSV.ini
│       │   ├── GSWE64.ini
│       │   ├── GSW.ini
│       │   ├── GSX.ini
│       │   ├── GSZ.ini
│       │   ├── GT3.ini
│       │   ├── GT6E70.ini
│       │   ├── GT6.ini
│       │   ├── GT7.ini
│       │   ├── GTEE01.ini
│       │   ├── GTEP01.ini
│       │   ├── GTKE51.ini
│       │   ├── GTK.ini
│       │   ├── GTO.ini
│       │   ├── GTOJAF.ini
│       │   ├── GTRE78r0.ini
│       │   ├── GTRE78r1.ini
│       │   ├── GTR.ini
│       │   ├── GTRJ8N.ini
│       │   ├── GTRP78.ini
│       │   ├── GTSE4F.ini
│       │   ├── GTY.ini
│       │   ├── GTZE41.ini
│       │   ├── GTZ.ini
│       │   ├── GTZP41.ini
│       │   ├── GU2D78.ini
│       │   ├── GU2F78.ini
│       │   ├── GU2.ini
│       │   ├── GU3D78.ini
│       │   ├── GU3.ini
│       │   ├── GU3X78.ini
│       │   ├── GU4.ini
│       │   ├── GU4Y78.ini
│       │   ├── GU6.ini
│       │   ├── GUB.ini
│       │   ├── GUM.ini
│       │   ├── GUNE5D.ini
│       │   ├── GUNE5Dr0.ini
│       │   ├── GUNE5Dr1.ini
│       │   ├── GUN.ini
│       │   ├── GUNP5D.ini
│       │   ├── GUP.ini
│       │   ├── GUT.ini
│       │   ├── GUZ.ini
│       │   ├── GV4E69.ini
│       │   ├── GVC.ini
│       │   ├── GVD.ini
│       │   ├── GVJE08.ini
│       │   ├── GVJ.ini
│       │   ├── GVJP08.ini
│       │   ├── GVL.ini
│       │   ├── GVO.ini
│       │   ├── GVPE69.ini
│       │   ├── GVSE8P.ini
│       │   ├── GVS.ini
│       │   ├── GW2.ini
│       │   ├── GW5E69.ini
│       │   ├── GW7.ini
│       │   ├── GW9.ini
│       │   ├── GWH.ini
│       │   ├── GWJ.ini
│       │   ├── GWK.ini
│       │   ├── GWL.ini
│       │   ├── GWP.ini
│       │   ├── GWQE52.ini
│       │   ├── GWRE01.ini
│       │   ├── GWR.ini
│       │   ├── GWRP01.ini
│       │   ├── GWT.ini
│       │   ├── GWWE01.ini
│       │   ├── GWWJ01.ini
│       │   ├── GWWP01.ini
│       │   ├── GWY.ini
│       │   ├── GWZE01.ini
│       │   ├── GX3.ini
│       │   ├── GXCE01.ini
│       │   ├── GXG.ini
│       │   ├── GXM.ini
│       │   ├── GXN.ini
│       │   ├── GXRP08.ini
│       │   ├── GXSE8P.ini
│       │   ├── GXS.ini
│       │   ├── GXSJ8P.ini
│       │   ├── GXSP8P.ini
│       │   ├── GXU.ini
│       │   ├── GXXE01.ini
│       │   ├── GXX.ini
│       │   ├── GXXJ01.ini
│       │   ├── GXXP01.ini
│       │   ├── GYA.ini
│       │   ├── GYFPA4.ini
│       │   ├── GYQ.ini
│       │   ├── GYT.ini
│       │   ├── GZ2E01.ini
│       │   ├── GZ2.ini
│       │   ├── GZ2J01.ini
│       │   ├── GZ2P01.ini
│       │   ├── GZ3E70.ini
│       │   ├── GZ3.ini
│       │   ├── GZB.ini
│       │   ├── GZBJB2.ini
│       │   ├── GZD.ini
│       │   ├── GZDP70.ini
│       │   ├── GZE.ini
│       │   ├── GZLE01.ini
│       │   ├── GZL.ini
│       │   ├── GZLJ01.ini
│       │   ├── GZLP01.ini
│       │   ├── GZPE70.ini
│       │   ├── GZP.ini
│       │   ├── GZPP70.ini
│       │   ├── GZSE70.ini
│       │   ├── GZW.ini
│       │   ├── HA8.ini
│       │   ├── HA9.ini
│       │   ├── HAA.ini
│       │   ├── HAB.ini
│       │   ├── HAC.ini
│       │   ├── HAF.ini
│       │   ├── HAG.ini
│       │   ├── HAJ.ini
│       │   ├── HAL.ini
│       │   ├── HATE01.ini
│       │   ├── HAT.ini
│       │   ├── HATJ01.ini
│       │   ├── HATP01.ini
│       │   ├── HAY.ini
│       │   ├── HBA.ini
│       │   ├── HBB.ini
│       │   ├── HBC.ini
│       │   ├── HBD.ini
│       │   ├── HBF.ini
│       │   ├── HBG.ini
│       │   ├── HBI.ini
│       │   ├── HBK.ini
│       │   ├── HC2.ini
│       │   ├── HC4.ini
│       │   ├── HCL.ini
│       │   ├── HCS.ini
│       │   ├── ID-gbihf.ini
│       │   ├── ID-gbi.ini
│       │   ├── ID-gbisr.ini
│       │   ├── JA7.ini
│       │   ├── JAE.ini
│       │   ├── JAL.ini
│       │   ├── JAP.ini
│       │   ├── JB6.ini
│       │   ├── JBA.ini
│       │   ├── JBC.ini
│       │   ├── JBH.ini
│       │   ├── JBK.ini
│       │   ├── JBO.ini
│       │   ├── JBQ.ini
│       │   ├── JBS.ini
│       │   ├── JBU.ini
│       │   ├── JC6.ini
│       │   ├── JC8.ini
│       │   ├── JC9.ini
│       │   ├── JCD.ini
│       │   ├── JCE.ini
│       │   ├── JCL.ini
│       │   ├── JCT.ini
│       │   ├── JCX.ini
│       │   ├── JCY.ini
│       │   ├── JDA.ini
│       │   ├── JDV.ini
│       │   ├── JEC.ini
│       │   ├── J.ini
│       │   ├── LAD.ini
│       │   ├── LAF.ini
│       │   ├── LAK.ini
│       │   ├── LAL.ini
│       │   ├── LAO.ini
│       │   ├── LAP.ini
│       │   ├── L.ini
│       │   ├── LULZHB.ini
│       │   ├── MAK.ini
│       │   ├── MB3.ini
│       │   ├── MB9.ini
│       │   ├── MBA.ini
│       │   ├── MCD.ini
│       │   ├── MCS.ini
│       │   ├── MCT.ini
│       │   ├── MCV.ini
│       │   ├── MCW.ini
│       │   ├── MCY.ini
│       │   ├── MCZ.ini
│       │   ├── M.ini
│       │   ├── NAB.ini
│       │   ├── NAC.ini
│       │   ├── NAD.ini
│       │   ├── NAE.ini
│       │   ├── NAF.ini
│       │   ├── NAH.ini
│       │   ├── NAK.ini
│       │   ├── NAL.ini
│       │   ├── NAO.ini
│       │   ├── NAR.ini
│       │   ├── NAT.ini
│       │   ├── N.ini
│       │   ├── P1RE01.ini
│       │   ├── P2M.ini
│       │   ├── P4B.ini
│       │   ├── PC6.ini
│       │   ├── PCK.ini
│       │   ├── PCS.ini
│       │   ├── PGS.ini
│       │   ├── P.ini
│       │   ├── PM4.ini
│       │   ├── PNR.ini
│       │   ├── PRJ.ini
│       │   ├── PZLE01.ini
│       │   ├── PZL.ini
│       │   ├── Q.ini
│       │   ├── R22.ini
│       │   ├── R25.ini
│       │   ├── R26.ini
│       │   ├── R29.ini
│       │   ├── R2E.ini
│       │   ├── R2F.ini
│       │   ├── R2G.ini
│       │   ├── R2H.ini
│       │   ├── R2L.ini
│       │   ├── R2M.ini
│       │   ├── R2P.ini
│       │   ├── R2Q.ini
│       │   ├── R2R.ini
│       │   ├── R2V.ini
│       │   ├── R2W.ini
│       │   ├── R32.ini
│       │   ├── R35.ini
│       │   ├── R38.ini
│       │   ├── R3A.ini
│       │   ├── R3C.ini
│       │   ├── R3D.ini
│       │   ├── R3E.ini
│       │   ├── R3G.ini
│       │   ├── R3H.ini
│       │   ├── R3I.ini
│       │   ├── R3J.ini
│       │   ├── R3M.ini
│       │   ├── R3N.ini
│       │   ├── R3O.ini
│       │   ├── R3R.ini
│       │   ├── R3S.ini
│       │   ├── R3X.ini
│       │   ├── R44.ini
│       │   ├── R46.ini
│       │   ├── R4C.ini
│       │   ├── R4D.ini
│       │   ├── R4E.ini
│       │   ├── R4F.ini
│       │   ├── R4L.ini
│       │   ├── R4M.ini
│       │   ├── R4QE01.ini
│       │   ├── R4QJ01.ini
│       │   ├── R4QK01.ini
│       │   ├── R4QP01r1.ini
│       │   ├── R4QP01r2.ini
│       │   ├── R4V.ini
│       │   ├── R4Z.ini
│       │   ├── R55.ini
│       │   ├── R58.ini
│       │   ├── R59.ini
│       │   ├── R5D.ini
│       │   ├── R5F.ini
│       │   ├── R5I.ini
│       │   ├── R5O.ini
│       │   ├── R5P.ini
│       │   ├── R5Q.ini
│       │   ├── R5S.ini
│       │   ├── R5T.ini
│       │   ├── R5W.ini
│       │   ├── R5X.ini
│       │   ├── R64.ini
│       │   ├── R66.ini
│       │   ├── R67.ini
│       │   ├── R6APPU.ini
│       │   ├── R6B.ini
│       │   ├── R6C.ini
│       │   ├── R6E.ini
│       │   ├── R6G.ini
│       │   ├── R6Q.ini
│       │   ├── R6T.ini
│       │   ├── R6V.ini
│       │   ├── R6X.ini
│       │   ├── R6Y.ini
│       │   ├── R74.ini
│       │   ├── R75.ini
│       │   ├── R77.ini
│       │   ├── R79.ini
│       │   ├── R7B.ini
│       │   ├── R7E.ini
│       │   ├── R7G.ini
│       │   ├── R7H.ini
│       │   ├── R7K.ini
│       │   ├── R7N.ini
│       │   ├── R7PE01.ini
│       │   ├── R7P.ini
│       │   ├── R7PP01.ini
│       │   ├── R7S.ini
│       │   ├── R7XE69.ini
│       │   ├── R7X.ini
│       │   ├── R7XJ13.ini
│       │   ├── R7XP69.ini
│       │   ├── R82.ini
│       │   ├── R84.ini
│       │   ├── R86.ini
│       │   ├── R88.ini
│       │   ├── R89.ini
│       │   ├── R8A.ini
│       │   ├── R8D.ini
│       │   ├── R8G.ini
│       │   ├── R8I.ini
│       │   ├── R8J.ini
│       │   ├── R8K.ini
│       │   ├── R8L.ini
│       │   ├── R8N.ini
│       │   ├── R8P.ini
│       │   ├── R8R.ini
│       │   ├── R8T.ini
│       │   ├── R92.ini
│       │   ├── R9B.ini
│       │   ├── R9D.ini
│       │   ├── R9E.ini
│       │   ├── R9G.ini
│       │   ├── R9I.ini
│       │   ├── R9Q.ini
│       │   ├── R9R.ini
│       │   ├── R9S.ini
│       │   ├── R9W.ini
│       │   ├── RAA.ini
│       │   ├── RB2.ini
│       │   ├── RB5.ini
│       │   ├── RB7E54.ini
│       │   ├── RB7.ini
│       │   ├── RB7P54.ini
│       │   ├── RB8.ini
│       │   ├── RB9.ini
│       │   ├── RBB.ini
│       │   ├── RBC.ini
│       │   ├── RBF.ini
│       │   ├── RBH.ini
│       │   ├── RBI.ini
│       │   ├── RBK.ini
│       │   ├── RBL.ini
│       │   ├── RBM.ini
│       │   ├── RBO.ini
│       │   ├── RBP.ini
│       │   ├── RBQ.ini
│       │   ├── RBR.ini
│       │   ├── RBS.ini
│       │   ├── RBT.ini
│       │   ├── RBW.ini
│       │   ├── RBY.ini
│       │   ├── RBZ.ini
│       │   ├── RC2.ini
│       │   ├── RC4.ini
│       │   ├── RC5.ini
│       │   ├── RCA.ini
│       │   ├── RCB.ini
│       │   ├── RCC.ini
│       │   ├── RCE.ini
│       │   ├── RCF.ini
│       │   ├── RCH.ini
│       │   ├── RCJ.ini
│       │   ├── RCK.ini
│       │   ├── RCL.ini
│       │   ├── RCO.ini
│       │   ├── RCP.ini
│       │   ├── RCS.ini
│       │   ├── RCT.ini
│       │   ├── RCU.ini
│       │   ├── RCV.ini
│       │   ├── RCY.ini
│       │   ├── RD2.ini
│       │   ├── RD8.ini
│       │   ├── RD9.ini
│       │   ├── RDA.ini
│       │   ├── RDB.ini
│       │   ├── RDF.ini
│       │   ├── RDJ.ini
│       │   ├── RDL.ini
│       │   ├── RDM.ini
│       │   ├── RDP.ini
│       │   ├── RDS.ini
│       │   ├── RDT.ini
│       │   ├── RDU.ini
│       │   ├── RDZ.ini
│       │   ├── RE8.ini
│       │   ├── REB.ini
│       │   ├── REF.ini
│       │   ├── REG.ini
│       │   ├── REL.ini
│       │   ├── REM.ini
│       │   ├── RENE8P.ini
│       │   ├── REP.ini
│       │   ├── REQ.ini
│       │   ├── RES.ini
│       │   ├── RET.ini
│       │   ├── REU.ini
│       │   ├── REX.ini
│       │   ├── REZ.ini
│       │   ├── RF2.ini
│       │   ├── RF4.ini
│       │   ├── RFA.ini
│       │   ├── RFB.ini
│       │   ├── RFC.ini
│       │   ├── RFF.ini
│       │   ├── RFK.ini
│       │   ├── RFN.ini
│       │   ├── RFP.ini
│       │   ├── RFQ.ini
│       │   ├── RFR.ini
│       │   ├── RFS.ini
│       │   ├── RFT.ini
│       │   ├── RFU.ini
│       │   ├── RFW.ini
│       │   ├── RG2.ini
│       │   ├── RG4.ini
│       │   ├── RG6.ini
│       │   ├── RG8.ini
│       │   ├── RGB.ini
│       │   ├── RGD.ini
│       │   ├── RGI.ini
│       │   ├── RGJ.ini
│       │   ├── RGK.ini
│       │   ├── RGM.ini
│       │   ├── RGN.ini
│       │   ├── RGQE70.ini
│       │   ├── RGQ.ini
│       │   ├── RGS.ini
│       │   ├── RGWE41.ini
│       │   ├── RGW.ini
│       │   ├── RGWP41.ini
│       │   ├── RGWX41r0.ini
│       │   ├── RGWX41r1.ini
│       │   ├── RGX.ini
│       │   ├── RGY.ini
│       │   ├── RH2.ini
│       │   ├── RH4.ini
│       │   ├── RH5.ini
│       │   ├── RH6.ini
│       │   ├── RH7.ini
│       │   ├── RH8.ini
│       │   ├── RH9.ini
│       │   ├── RHA.ini
│       │   ├── RHC.ini
│       │   ├── RHD.ini
│       │   ├── RHE.ini
│       │   ├── RHF.ini
│       │   ├── RHG.ini
│       │   ├── RHJ.ini
│       │   ├── RHL.ini
│       │   ├── RHM.ini
│       │   ├── RHN.ini
│       │   ├── RHO.ini
│       │   ├── RHP.ini
│       │   ├── RHR.ini
│       │   ├── RHT.ini
│       │   ├── RHV.ini
│       │   ├── RHZ.ini
│       │   ├── RI2.ini
│       │   ├── RI3.ini
│       │   ├── RI7.ini
│       │   ├── RI8.ini
│       │   ├── RIE.ini
│       │   ├── RIF.ini
│       │   ├── RIG.ini
│       │   ├── RIL.ini
│       │   ├── RIM.ini
│       │   ├── RIP.ini
│       │   ├── RIR.ini
│       │   ├── RIU.ini
│       │   ├── RIZ.ini
│       │   ├── RJ2E52.ini
│       │   ├── RJ2.ini
│       │   ├── RJ2JGD.ini
│       │   ├── RJ2P52.ini
│       │   ├── RJ3.ini
│       │   ├── RJ4.ini
│       │   ├── RJ7.ini
│       │   ├── RJ8.ini
│       │   ├── RJB.ini
│       │   ├── RJC.ini
│       │   ├── RJE.ini
│       │   ├── RJF.ini
│       │   ├── RJN.ini
│       │   ├── RJQ.ini
│       │   ├── RJS.ini
│       │   ├── RJZ.ini
│       │   ├── RK2.ini
│       │   ├── RK9.ini
│       │   ├── RKA.ini
│       │   ├── RKD.ini
│       │   ├── RKF.ini
│       │   ├── RKG.ini
│       │   ├── RKI.ini
│       │   ├── RKJ.ini
│       │   ├── RKL.ini
│       │   ├── RKM.ini
│       │   ├── RKP.ini
│       │   ├── RKQ.ini
│       │   ├── RKS.ini
│       │   ├── RKT.ini
│       │   ├── RKW.ini
│       │   ├── RL5.ini
│       │   ├── RL6.ini
│       │   ├── RLD.ini
│       │   ├── RLEEFS.ini
│       │   ├── RLI.ini
│       │   ├── RLJ.ini
│       │   ├── RLK.ini
│       │   ├── RLL.ini
│       │   ├── RLS.ini
│       │   ├── RLT.ini
│       │   ├── RLV.ini
│       │   ├── RLX.ini
│       │   ├── RM3.ini
│       │   ├── RM4.ini
│       │   ├── RM7.ini
│       │   ├── RM8E01.ini
│       │   ├── RM8.ini
│       │   ├── RM8J01.ini
│       │   ├── RM8P01.ini
│       │   ├── RM9.ini
│       │   ├── RMCE01.ini
│       │   ├── RMC.ini
│       │   ├── RMCJ01.ini
│       │   ├── RMCK01.ini
│       │   ├── RMCP01.ini
│       │   ├── RME.ini
│       │   ├── RMG.ini
│       │   ├── RMHE08.ini
│       │   ├── RMH.ini
│       │   ├── RMHJ08.ini
│       │   ├── RMHP08.ini
│       │   ├── RMI.ini
│       │   ├── RMJ.ini
│       │   ├── RMK.ini
│       │   ├── RML.ini
│       │   ├── RMO.ini
│       │   ├── RMP.ini
│       │   ├── RMQ.ini
│       │   ├── RMR.ini
│       │   ├── RMT.ini
│       │   ├── RMV.ini
│       │   ├── RMW.ini
│       │   ├── RMY.ini
│       │   ├── RMZ.ini
│       │   ├── RN2.ini
│       │   ├── RN3.ini
│       │   ├── RN5.ini
│       │   ├── RN8.ini
│       │   ├── RNB.ini
│       │   ├── RNC.ini
│       │   ├── RND.ini
│       │   ├── RNG.ini
│       │   ├── RNK.ini
│       │   ├── RNM.ini
│       │   ├── RNO.ini
│       │   ├── RNSE69.ini
│       │   ├── RNU.ini
│       │   ├── RNV.ini
│       │   ├── RNW.ini
│       │   ├── RNX.ini
│       │   ├── RO2P7N.ini
│       │   ├── RO3.ini
│       │   ├── RO7.ini
│       │   ├── RO8.ini
│       │   ├── RO9.ini
│       │   ├── ROA.ini
│       │   ├── ROB.ini
│       │   ├── ROC.ini
│       │   ├── ROD.ini
│       │   ├── ROE.ini
│       │   ├── ROF.ini
│       │   ├── ROG.ini
│       │   ├── ROL.ini
│       │   ├── ROM.ini
│       │   ├── RON.ini
│       │   ├── ROO.ini
│       │   ├── ROP.ini
│       │   ├── ROT.ini
│       │   ├── ROU.ini
│       │   ├── ROW.ini
│       │   ├── ROX.ini
│       │   ├── RPBE01.ini
│       │   ├── RPB.ini
│       │   ├── RPBJ01.ini
│       │   ├── RPBJ01r0.ini
│       │   ├── RPBJ01r1.ini
│       │   ├── RPBJ01r2.ini
│       │   ├── RPBP01.ini
│       │   ├── RPC.ini
│       │   ├── RPD.ini
│       │   ├── RPF.ini
│       │   ├── RPG.ini
│       │   ├── RPH.ini
│       │   ├── RPJ.ini
│       │   ├── RPK.ini
│       │   ├── RPL.ini
│       │   ├── RPM.ini
│       │   ├── RPO.ini
│       │   ├── RPP.ini
│       │   ├── RPQ.ini
│       │   ├── RPS.ini
│       │   ├── RPT.ini
│       │   ├── RPU.ini
│       │   ├── RPY.ini
│       │   ├── RQ2.ini
│       │   ├── RQ4.ini
│       │   ├── RQ5.ini
│       │   ├── RQ6.ini
│       │   ├── RQ8.ini
│       │   ├── RQB.ini
│       │   ├── RQE.ini
│       │   ├── RQF.ini
│       │   ├── RQL.ini
│       │   ├── RQM.ini
│       │   ├── RQN.ini
│       │   ├── RQP.ini
│       │   ├── RQQ.ini
│       │   ├── RQR.ini
│       │   ├── RQS.ini
│       │   ├── RQT.ini
│       │   ├── RQU.ini
│       │   ├── RQW.ini
│       │   ├── RQZ.ini
│       │   ├── RR2.ini
│       │   ├── RR3.ini
│       │   ├── RR5.ini
│       │   ├── RRA.ini
│       │   ├── RRBE41r0.ini
│       │   ├── RRBE41r1.ini
│       │   ├── RRBE41r2.ini
│       │   ├── RRB.ini
│       │   ├── RRBJ41.ini
│       │   ├── RRBP41.ini
│       │   ├── RRF.ini
│       │   ├── RRK.ini
│       │   ├── RRL.ini
│       │   ├── RRO.ini
│       │   ├── RRP.ini
│       │   ├── RRS.ini
│       │   ├── RRT.ini
│       │   ├── RRV.ini
│       │   ├── RRW.ini
│       │   ├── RRX.ini
│       │   ├── RRZ.ini
│       │   ├── RS2.ini
│       │   ├── RS4.ini
│       │   ├── RS5.ini
│       │   ├── RSA.ini
│       │   ├── RSBE01.ini
│       │   ├── RSB.ini
│       │   ├── RSBP01.ini
│       │   ├── RSD.ini
│       │   ├── RSH.ini
│       │   ├── RSI.ini
│       │   ├── RSJ.ini
│       │   ├── RSL.ini
│       │   ├── RSM.ini
│       │   ├── RSN.ini
│       │   ├── RSO.ini
│       │   ├── RSP.ini
│       │   ├── RSRE8P.ini
│       │   ├── RSR.ini
│       │   ├── RSS.ini
│       │   ├── RST.ini
│       │   ├── RSVE8P.ini
│       │   ├── RSX.ini
│       │   ├── RSY.ini
│       │   ├── RT3.ini
│       │   ├── RT4.ini
│       │   ├── RT7.ini
│       │   ├── RT8.ini
│       │   ├── RTB.ini
│       │   ├── RTC.ini
│       │   ├── RTG.ini
│       │   ├── RTH.ini
│       │   ├── RTJ.ini
│       │   ├── RTK.ini
│       │   ├── RTL.ini
│       │   ├── RTM.ini
│       │   ├── RTP.ini
│       │   ├── RTQ.ini
│       │   ├── RTR.ini
│       │   ├── RTT.ini
│       │   ├── RTU.ini
│       │   ├── RTW.ini
│       │   ├── RTZ.ini
│       │   ├── RU4.ini
│       │   ├── RUA.ini
│       │   ├── RUD.ini
│       │   ├── RUFEMV.ini
│       │   ├── RUF.ini
│       │   ├── RUFP99.ini
│       │   ├── RUN.ini
│       │   ├── RUO.ini
│       │   ├── RUP.ini
│       │   ├── RUR.ini
│       │   ├── RUS.ini
│       │   ├── RUUE01r0.ini
│       │   ├── RUUE01r1.ini
│       │   ├── RUU.ini
│       │   ├── RUUJ01r1.ini
│       │   ├── RUUK01r1.ini
│       │   ├── RUUP01r0.ini
│       │   ├── RUUP01r1.ini
│       │   ├── RUW.ini
│       │   ├── RUZ.ini
│       │   ├── RV2.ini
│       │   ├── RVA.ini
│       │   ├── RVB.ini
│       │   ├── RVC.ini
│       │   ├── RVE.ini
│       │   ├── RVN.ini
│       │   ├── RVO.ini
│       │   ├── RVQ.ini
│       │   ├── RVR.ini
│       │   ├── RW3.ini
│       │   ├── RW4.ini
│       │   ├── RW7.ini
│       │   ├── RW8.ini
│       │   ├── RWA.ini
│       │   ├── RWB.ini
│       │   ├── RWC.ini
│       │   ├── RWF.ini
│       │   ├── RWG.ini
│       │   ├── RWH.ini
│       │   ├── RWK.ini
│       │   ├── RWN.ini
│       │   ├── RWO.ini
│       │   ├── RWQ.ini
│       │   ├── RWS.ini
│       │   ├── RWY.ini
│       │   ├── RWZ.ini
│       │   ├── RX3.ini
│       │   ├── RX4E4Z.ini
│       │   ├── RX4.ini
│       │   ├── RX4PMT.ini
│       │   ├── RX6.ini
│       │   ├── RXB.ini
│       │   ├── RXC.ini
│       │   ├── RXF.ini
│       │   ├── RXH.ini
│       │   ├── RXI.ini
│       │   ├── RXR.ini
│       │   ├── RXV.ini
│       │   ├── RXX.ini
│       │   ├── RXZ.ini
│       │   ├── RY2.ini
│       │   ├── RY3.ini
│       │   ├── RY4.ini
│       │   ├── RY8.ini
│       │   ├── RYB.ini
│       │   ├── RYG.ini
│       │   ├── RYH.ini
│       │   ├── RYI.ini
│       │   ├── RYL.ini
│       │   ├── RYN.ini
│       │   ├── RYV.ini
│       │   ├── RYW.ini
│       │   ├── RYZ.ini
│       │   ├── RZ2.ini
│       │   ├── RZ3.ini
│       │   ├── RZ4.ini
│       │   ├── RZ5.ini
│       │   ├── RZ6.ini
│       │   ├── RZ7.ini
│       │   ├── RZ8.ini
│       │   ├── RZDE01r0.ini
│       │   ├── RZDE01r2.ini
│       │   ├── RZD.ini
│       │   ├── RZDJ01.ini
│       │   ├── RZDK01.ini
│       │   ├── RZDP01.ini
│       │   ├── RZF.ini
│       │   ├── RZI.ini
│       │   ├── RZJ.ini
│       │   ├── RZJP69.ini
│       │   ├── RZL.ini
│       │   ├── RZO.ini
│       │   ├── RZR.ini
│       │   ├── RZT.ini
│       │   ├── RZY.ini
│       │   ├── S25.ini
│       │   ├── S2C.ini
│       │   ├── S2D.ini
│       │   ├── S2E.ini
│       │   ├── S2L.ini
│       │   ├── S2O.ini
│       │   ├── S2P.ini
│       │   ├── S2W.ini
│       │   ├── S3B.ini
│       │   ├── S3C.ini
│       │   ├── S3H.ini
│       │   ├── S3I.ini
│       │   ├── S59.ini
│       │   ├── S5D.ini
│       │   ├── S5M.ini
│       │   ├── S5S.ini
│       │   ├── S72.ini
│       │   ├── S75.ini
│       │   ├── S7B.ini
│       │   ├── S7E.ini
│       │   ├── SAA.ini
│       │   ├── SAG.ini
│       │   ├── SAH.ini
│       │   ├── SAK.ini
│       │   ├── SAL.ini
│       │   ├── SAN.ini
│       │   ├── SAOE78.ini
│       │   ├── SAOEVZ.ini
│       │   ├── SAT.ini
│       │   ├── SB3.ini
│       │   ├── SB4.ini
│       │   ├── SB8.ini
│       │   ├── SBD.ini
│       │   ├── SBE.ini
│       │   ├── SBF.ini
│       │   ├── SBK.ini
│       │   ├── SBLE5G.ini
│       │   ├── SBLP5G.ini
│       │   ├── SBQ.ini
│       │   ├── SBR.ini
│       │   ├── SBV.ini
│       │   ├── SBX.ini
│       │   ├── SBY.ini
│       │   ├── SBZ.ini
│       │   ├── SC2E8P.ini
│       │   ├── SC2.ini
│       │   ├── SC7.ini
│       │   ├── SCA.ini
│       │   ├── SCD.ini
│       │   ├── SCE.ini
│       │   ├── SCF.ini
│       │   ├── SCH.ini
│       │   ├── SCI.ini
│       │   ├── SCK.ini
│       │   ├── SCT.ini
│       │   ├── SCYE4Q.ini
│       │   ├── SCY.ini
│       │   ├── SCYP4Q.ini
│       │   ├── SCYR4Q.ini
│       │   ├── SCYX4Q.ini
│       │   ├── SCYY4Q.ini
│       │   ├── SCYZ4Q.ini
│       │   ├── SD2.ini
│       │   ├── SD2J01.ini
│       │   ├── SD8.ini
│       │   ├── SDA.ini
│       │   ├── SDB.ini
│       │   ├── SDE.ini
│       │   ├── SDL.ini
│       │   ├── SDM.ini
│       │   ├── SDN.ini
│       │   ├── SDO.ini
│       │   ├── SDVE41.ini
│       │   ├── SDV.ini
│       │   ├── SDVP41.ini
│       │   ├── SDW.ini
│       │   ├── SDZ.ini
│       │   ├── SE2.ini
│       │   ├── SEA.ini
│       │   ├── SEC.ini
│       │   ├── SEG.ini
│       │   ├── SEM.ini
│       │   ├── SEP.ini
│       │   ├── SER.ini
│       │   ├── SEU.ini
│       │   ├── SEV.ini
│       │   ├── SF2.ini
│       │   ├── SF7.ini
│       │   ├── SF8.ini
│       │   ├── SFI.ini
│       │   ├── SFP.ini
│       │   ├── SFR.ini
│       │   ├── SFU.ini
│       │   ├── SG2.ini
│       │   ├── SG3.ini
│       │   ├── SG7.ini
│       │   ├── SG8.ini
│       │   ├── SGD.ini
│       │   ├── SGLEA4.ini
│       │   ├── SGL.ini
│       │   ├── SGLPA4.ini
│       │   ├── SGT.ini
│       │   ├── SGV.ini
│       │   ├── SGX.ini
│       │   ├── SH2.ini
│       │   ├── SH6.ini
│       │   ├── SH8.ini
│       │   ├── SH9.ini
│       │   ├── SHL.ini
│       │   ├── SHO.ini
│       │   ├── SHP.ini
│       │   ├── SHU.ini
│       │   ├── SHW.ini
│       │   ├── SHX.ini
│       │   ├── SIL.ini
│       │   ├── SIS.ini
│       │   ├── SJ2.ini
│       │   ├── SJ6.ini
│       │   ├── SJ7.ini
│       │   ├── SJ9.ini
│       │   ├── SJB.ini
│       │   ├── SJC.ini
│       │   ├── SJD.ini
│       │   ├── SJDJ01.ini
│       │   ├── SJE.ini
│       │   ├── SJHE41.ini
│       │   ├── SJK.ini
│       │   ├── SJL.ini
│       │   ├── SJQ.ini
│       │   ├── SJTP41.ini
│       │   ├── SJX.ini
│       │   ├── SJZ.ini
│       │   ├── SK3.ini
│       │   ├── SK4.ini
│       │   ├── SK8.ini
│       │   ├── SKA.ini
│       │   ├── SKB.ini
│       │   ├── SKC.ini
│       │   ├── SKG.ini
│       │   ├── SKJ.ini
│       │   ├── SKO.ini
│       │   ├── SKP.ini
│       │   ├── SKT.ini
│       │   ├── SKU.ini
│       │   ├── SKV.ini
│       │   ├── SKW.ini
│       │   ├── SKX.ini
│       │   ├── SKY.ini
│       │   ├── SL2.ini
│       │   ├── SL2P01.ini
│       │   ├── SLE.ini
│       │   ├── SLP.ini
│       │   ├── SLS.ini
│       │   ├── SLSP01.ini
│       │   ├── SLT.ini
│       │   ├── SLW.ini
│       │   ├── SM2.ini
│       │   ├── SM6.ini
│       │   ├── SMB.ini
│       │   ├── SMF.ini
│       │   ├── SMI.ini
│       │   ├── SMM.ini
│       │   ├── SMNE01.ini
│       │   ├── SMN.ini
│       │   ├── SMNP01.ini
│       │   ├── SMO.ini
│       │   ├── SMS.ini
│       │   ├── SMU.ini
│       │   ├── SMZ.ini
│       │   ├── SN2.ini
│       │   ├── SND.ini
│       │   ├── SNG.ini
│       │   ├── SNJE69.ini
│       │   ├── SNJ.ini
│       │   ├── SNM.ini
│       │   ├── SNQ.ini
│       │   ├── SNS.ini
│       │   ├── SNT.ini
│       │   ├── SNY.ini
│       │   ├── SOC.ini
│       │   ├── SOD.ini
│       │   ├── SOJ.ini
│       │   ├── SOM.ini
│       │   ├── SON.ini
│       │   ├── SOR.ini
│       │   ├── SOS.ini
│       │   ├── SOU.ini
│       │   ├── SP3.ini
│       │   ├── SP4.ini
│       │   ├── SP7.ini
│       │   ├── SP8.ini
│       │   ├── SP9.ini
│       │   ├── SPA.ini
│       │   ├── SPC.ini
│       │   ├── SPD.ini
│       │   ├── SPH.ini
│       │   ├── SPM.ini
│       │   ├── SPQ.ini
│       │   ├── SPR.ini
│       │   ├── SPT.ini
│       │   ├── SPU.ini
│       │   ├── SPV.ini
│       │   ├── SPZ.ini
│       │   ├── SQD.ini
│       │   ├── SQIE4Q.ini
│       │   ├── SQI.ini
│       │   ├── SQIP4Q.ini
│       │   ├── SQIY4Q.ini
│       │   ├── SR4.ini
│       │   ├── SR5.ini
│       │   ├── SR6.ini
│       │   ├── SR7.ini
│       │   ├── SR8.ini
│       │   ├── SR9.ini
│       │   ├── SRA.ini
│       │   ├── SRE.ini
│       │   ├── SRL.ini
│       │   ├── SRQ.ini
│       │   ├── SRT.ini
│       │   ├── SRV.ini
│       │   ├── SRW.ini
│       │   ├── SRX.ini
│       │   ├── SS8.ini
│       │   ├── SS9.ini
│       │   ├── SSC.ini
│       │   ├── SSG.ini
│       │   ├── SSH.ini
│       │   ├── SSP.ini
│       │   ├── SSQ.ini
│       │   ├── SSR.ini
│       │   ├── SST.ini
│       │   ├── SSZ.ini
│       │   ├── ST4.ini
│       │   ├── ST6.ini
│       │   ├── ST7P01.ini
│       │   ├── STM.ini
│       │   ├── STN.ini
│       │   ├── STR.ini
│       │   ├── STSE4Q.ini
│       │   ├── STS.ini
│       │   ├── STSP4Qr1.ini
│       │   ├── STSP4Qr2.ini
│       │   ├── STSX4Q.ini
│       │   ├── STSY4Qr0.ini
│       │   ├── STSY4Qr1.ini
│       │   ├── STSZ4Q.ini
│       │   ├── STV.ini
│       │   ├── STZ.ini
│       │   ├── SU3.ini
│       │   ├── SU4.ini
│       │   ├── SU5.ini
│       │   ├── SU7.ini
│       │   ├── SUKE01.ini
│       │   ├── SUKJ01.ini
│       │   ├── SUKP01.ini
│       │   ├── SUM.ini
│       │   ├── SUO.ini
│       │   ├── SUS.ini
│       │   ├── SUU.ini
│       │   ├── SUV.ini
│       │   ├── SUW.ini
│       │   ├── SUX.ini
│       │   ├── SVB.ini
│       │   ├── SVF.ini
│       │   ├── SVM.ini
│       │   ├── SVV.ini
│       │   ├── SVW.ini
│       │   ├── SVZ.ini
│       │   ├── SW4.ini
│       │   ├── SX3.ini
│       │   ├── SX4E01.ini
│       │   ├── SX4.ini
│       │   ├── SX7.ini
│       │   ├── SX8.ini
│       │   ├── SXC.ini
│       │   ├── SZB.ini
│       │   ├── UGP.ini
│       │   ├── W22.ini
│       │   ├── W2G.ini
│       │   ├── W2L.ini
│       │   ├── W34.ini
│       │   ├── W3B.ini
│       │   ├── W3G.ini
│       │   ├── W3M.ini
│       │   ├── W4A.ini
│       │   ├── W4O.ini
│       │   ├── W5I.ini
│       │   ├── W64.ini
│       │   ├── W69.ini
│       │   ├── W8I.ini
│       │   ├── W8L.ini
│       │   ├── W8X.ini
│       │   ├── W9L.ini
│       │   ├── WA2.ini
│       │   ├── WAF.ini
│       │   ├── WAN.ini
│       │   ├── WAZ.ini
│       │   ├── WB2.ini
│       │   ├── WB3.ini
│       │   ├── WB4.ini
│       │   ├── WB6.ini
│       │   ├── WB7.ini
│       │   ├── WB8.ini
│       │   ├── WBA.ini
│       │   ├── WBI.ini
│       │   ├── WBK.ini
│       │   ├── WBL.ini
│       │   ├── WBR.ini
│       │   ├── WBV.ini
│       │   ├── WBX.ini
│       │   ├── WBY.ini
│       │   ├── WBZ.ini
│       │   ├── WC2.ini
│       │   ├── WC6.ini
│       │   ├── WCH.ini
│       │   ├── WCI.ini
│       │   ├── WCJ.ini
│       │   ├── WCO.ini
│       │   ├── WCP.ini
│       │   ├── WCU.ini
│       │   ├── WCV.ini
│       │   ├── WCZ.ini
│       │   ├── WD9.ini
│       │   ├── WDA.ini
│       │   ├── WDE.ini
│       │   ├── WDF.ini
│       │   ├── WDN.ini
│       │   ├── WDO.ini
│       │   ├── WDX.ini
│       │   ├── WEM.ini
│       │   ├── WF3.ini
│       │   ├── WF4.ini
│       │   ├── WF5.ini
│       │   ├── WFA.ini
│       │   ├── WFH.ini
│       │   ├── WFI.ini
│       │   ├── WFK.ini
│       │   ├── WFL.ini
│       │   ├── WFM.ini
│       │   ├── WFN.ini
│       │   ├── WFU.ini
│       │   ├── WFY.ini
│       │   ├── WGG.ini
│       │   ├── WGL.ini
│       │   ├── WGS.ini
│       │   ├── WGU.ini
│       │   ├── WH3.ini
│       │   ├── WHE.ini
│       │   ├── WHF.ini
│       │   ├── WHO.ini
│       │   ├── WHP.ini
│       │   ├── WHU.ini
│       │   ├── WHW.ini
│       │   ├── WHY.ini
│       │   ├── WIB.ini
│       │   ├── WIC.ini
│       │   ├── WIN.ini
│       │   ├── WIT.ini
│       │   ├── WJA.ini
│       │   ├── WJE.ini
│       │   ├── WJS.ini
│       │   ├── WKD.ini
│       │   ├── WKE.ini
│       │   ├── WKI.ini
│       │   ├── WKK.ini
│       │   ├── WKN.ini
│       │   ├── WKT.ini
│       │   ├── WKU.ini
│       │   ├── WKW.ini
│       │   ├── WL9.ini
│       │   ├── WLC.ini
│       │   ├── WLD.ini
│       │   ├── WLE.ini
│       │   ├── WLJ.ini
│       │   ├── WLK.ini
│       │   ├── WLM.ini
│       │   ├── WLN.ini
│       │   ├── WLO.ini
│       │   ├── WLP.ini
│       │   ├── WLT.ini
│       │   ├── WLX.ini
│       │   ├── WLZ.ini
│       │   ├── WM4.ini
│       │   ├── WM5.ini
│       │   ├── WM9.ini
│       │   ├── WMA.ini
│       │   ├── WMB.ini
│       │   ├── WMD.ini
│       │   ├── WMG.ini
│       │   ├── WML.ini
│       │   ├── WMOEE9.ini
│       │   ├── WMO.ini
│       │   ├── WMOJE9.ini
│       │   ├── WMOPE9.ini
│       │   ├── WMS.ini
│       │   ├── WMZ.ini
│       │   ├── WO6.ini
│       │   ├── WOA.ini
│       │   ├── WOD.ini
│       │   ├── WOF.ini
│       │   ├── WOG.ini
│       │   ├── WOL.ini
│       │   ├── WOP.ini
│       │   ├── WOX.ini
│       │   ├── WOY.ini
│       │   ├── WP4.ini
│       │   ├── WP6.ini
│       │   ├── WP9.ini
│       │   ├── WPA.ini
│       │   ├── WPB.ini
│       │   ├── WPD.ini
│       │   ├── WPF.ini
│       │   ├── WPH.ini
│       │   ├── WPJ.ini
│       │   ├── WPK.ini
│       │   ├── WPN.ini
│       │   ├── WPP.ini
│       │   ├── WPQ.ini
│       │   ├── WPS.ini
│       │   ├── WPT.ini
│       │   ├── WPU.ini
│       │   ├── WPX.ini
│       │   ├── WPZ.ini
│       │   ├── WQ4.ini
│       │   ├── WR2E41.ini
│       │   ├── WR2.ini
│       │   ├── WR2P41.ini
│       │   ├── WR5.ini
│       │   ├── WR9.ini
│       │   ├── WRA.ini
│       │   ├── WRD.ini
│       │   ├── WRF.ini
│       │   ├── WRI.ini
│       │   ├── WRS.ini
│       │   ├── WRX.ini
│       │   ├── WS2.ini
│       │   ├── WS3.ini
│       │   ├── WS4.ini
│       │   ├── WS5.ini
│       │   ├── WS6.ini
│       │   ├── WS9.ini
│       │   ├── WSH.ini
│       │   ├── WSI.ini
│       │   ├── WSL.ini
│       │   ├── WSR.ini
│       │   ├── WSS.ini
│       │   ├── WSX.ini
│       │   ├── WT8.ini
│       │   ├── WTB.ini
│       │   ├── WTD.ini
│       │   ├── WTE.ini
│       │   ├── WTI.ini
│       │   ├── WTK.ini
│       │   ├── WTN.ini
│       │   ├── WTU.ini
│       │   ├── WTX.ini
│       │   ├── WUK.ini
│       │   ├── WW2.ini
│       │   ├── WW3.ini
│       │   ├── WWA.ini
│       │   ├── WWI.ini
│       │   ├── WWX.ini
│       │   ├── WXB.ini
│       │   ├── WXP.ini
│       │   ├── WXR.ini
│       │   ├── WYM.ini
│       │   ├── WZB.ini
│       │   ├── WZG.ini
│       │   ├── WZI.ini
│       │   ├── WZM.ini
│       │   ├── XAA.ini
│       │   ├── XAB.ini
│       │   ├── XAD.ini
│       │   ├── XAE.ini
│       │   ├── XAF.ini
│       │   ├── XAG.ini
│       │   ├── XAH.ini
│       │   ├── XAI.ini
│       │   ├── XAK.ini
│       │   ├── XAL.ini
│       │   ├── XAM.ini
│       │   ├── XAN.ini
│       │   ├── XAO.ini
│       │   ├── XAP.ini
│       │   ├── XAQ.ini
│       │   ├── XH2.ini
│       │   ├── XH7.ini
│       │   ├── XH9.ini
│       │   ├── XHD.ini
│       │   ├── XHL.ini
│       │   ├── XHR.ini
│       │   ├── XI9.ini
│       │   ├── XIN.ini
│       │   ├── XIO.ini
│       │   ├── XIP.ini
│       │   ├── XIT.ini
│       │   ├── XIU.ini
│       │   └── XIV.ini
│       ├── GC
│       │   ├── dsp_coef.bin
│       │   ├── dsp_rom.bin
│       │   ├── font_japanese.bin
│       │   ├── font-licenses.txt
│       │   └── font_western.bin
│       ├── Load
│       │   └── GraphicMods
│       │       ├── All Games Bloom Removal
│       │       │   ├── all.txt
│       │       │   └── metadata.json
│       │       ├── All Games Blurred Bloom
│       │       │   ├── all.txt
│       │       │   ├── blur_horizontal.rastermaterial
│       │       │   ├── blur.ps.glsl
│       │       │   ├── blur.rastershader
│       │       │   ├── blur_vertical.rastermaterial
│       │       │   ├── blur.vs.glsl
│       │       │   └── metadata.json
│       │       ├── All Games Blurred DOF
│       │       │   ├── all.txt
│       │       │   ├── blur_horizontal.rastermaterial
│       │       │   ├── blur.ps.glsl
│       │       │   ├── blur.rastershader
│       │       │   ├── blur_vertical.rastermaterial
│       │       │   ├── blur.vs.glsl
│       │       │   └── metadata.json
│       │       ├── All Games DOF Removal
│       │       │   ├── all.txt
│       │       │   └── metadata.json
│       │       ├── All Games HUD Removal
│       │       │   ├── all.txt
│       │       │   └── metadata.json
│       │       ├── All Games Native Resolution Bloom
│       │       │   ├── all.txt
│       │       │   └── metadata.json
│       │       ├── All Games Native Resolution DOF
│       │       │   ├── all.txt
│       │       │   └── metadata.json
│       │       ├── Arc Rise Fantasia
│       │       │   ├── metadata.json
│       │       │   └── RPJ.txt
│       │       ├── Battalion Wars 2
│       │       │   ├── metadata.json
│       │       │   └── RBW.txt
│       │       ├── Conduit 2
│       │       │   ├── metadata.json
│       │       │   └── SC2.txt
│       │       ├── De Blob
│       │       │   ├── Bloom Blurred
│       │       │   │   ├── metadata.json
│       │       │   │   └── R6B.txt
│       │       │   └── Bloom Removal
│       │       │       ├── metadata.json
│       │       │       └── R6B.txt
│       │       ├── De Blob 2
│       │       │   ├── Bloom Blurred
│       │       │   │   ├── metadata.json
│       │       │   │   └── SDB.txt
│       │       │   └── Bloom Removal
│       │       │       ├── metadata.json
│       │       │       └── SDB.txt
│       │       ├── Donkey Kong Country Returns
│       │       │   ├── metadata.json
│       │       │   └── SF8.txt
│       │       ├── Dragon Ball Z Budokai Tenkaichi 3
│       │       │   ├── metadata.json
│       │       │   └── RDS.txt
│       │       ├── Epic Mickey
│       │       │   ├── metadata.json
│       │       │   └── SEM.txt
│       │       ├── Epic Mickey 2
│       │       │   ├── metadata.json
│       │       │   └── SER.txt
│       │       ├── Fragile Dreams - Farewell Ruins of the Moon
│       │       │   ├── metadata.json
│       │       │   └── R2G.txt
│       │       ├── Go Vacation
│       │       │   ├── metadata.json
│       │       │   └── SGV.txt
│       │       ├── Lego Batman
│       │       │   ├── metadata.json
│       │       │   └── RLB.txt
│       │       ├── Link's Crossbow Training
│       │       │   ├── metadata.json
│       │       │   └── RZP.txt
│       │       ├── Little King's Story
│       │       │   ├── metadata.json
│       │       │   └── RO3.txt
│       │       ├── Lord of the Rings Aragorns Quest
│       │       │   ├── metadata.json
│       │       │   └── R8J.txt
│       │       ├── LostWinds
│       │       │   ├── metadata.json
│       │       │   └── WLW.txt
│       │       ├── LostWinds - Winter of the Melodias
│       │       │   ├── metadata.json
│       │       │   └── WLO.txt
│       │       ├── Mario Kart Wii
│       │       │   ├── metadata.json
│       │       │   └── RMC.txt
│       │       ├── Mario Strikers Charged
│       │       │   ├── metadata.json
│       │       │   └── R4Q.txt
│       │       ├── Metroid Other M
│       │       │   ├── metadata.json
│       │       │   └── R3O.txt
│       │       ├── Metroid Prime 3 - Corruption
│       │       │   ├── metadata.json
│       │       │   └── RM3.txt
│       │       ├── Metroid Prime Trilogy
│       │       │   ├── metadata.json
│       │       │   └── R3M.txt
│       │       ├── Monster Hunter Tri
│       │       │   ├── DMH.txt
│       │       │   ├── metadata.json
│       │       │   └── RMH.txt
│       │       ├── Need for Speed Nitro
│       │       │   ├── metadata.json
│       │       │   └── R7X.txt
│       │       ├── Nights Journey of Dreams
│       │       │   ├── metadata.json
│       │       │   └── R7E.txt
│       │       ├── Okami
│       │       │   ├── metadata.json
│       │       │   └── ROW.txt
│       │       ├── Overlord Dark Legend
│       │       │   ├── metadata.json
│       │       │   └── ROA.txt
│       │       ├── Pandora's Tower
│       │       │   ├── metadata.json
│       │       │   └── SX3.txt
│       │       ├── Rune Factory Frontier
│       │       │   ├── metadata.json
│       │       │   └── RUF.txt
│       │       ├── Samurai Warriors 3
│       │       │   ├── metadata.json
│       │       │   └── S59.txt
│       │       ├── Samurai Warriors 3 Xtreme Legends
│       │       │   ├── metadata.json
│       │       │   └── S5Q.txt
│       │       ├── Sin and Punishment - Star Successor
│       │       │   ├── metadata.json
│       │       │   └── R2V.txt
│       │       ├── Skylanders Giants
│       │       │   ├── metadata.json
│       │       │   └── SKY.txt
│       │       ├── Skylanders Spyro's Adventure
│       │       │   ├── metadata.json
│       │       │   └── SSP.txt
│       │       ├── Skyward Sword Bloom
│       │       │   ├── metadata.json
│       │       │   └── SOU.txt
│       │       ├── Sonic Colors
│       │       │   ├── metadata.json
│       │       │   └── SNC.txt
│       │       ├── Sonic Unleashed
│       │       │   ├── metadata.json
│       │       │   └── RSV.txt
│       │       ├── Spectrobes Origins
│       │       │   ├── metadata.json
│       │       │   └── RXX.txt
│       │       ├── Spyborgs
│       │       │   ├── metadata.json
│       │       │   └── RSW.txt
│       │       ├── Super Mario Galaxy
│       │       │   ├── metadata.json
│       │       │   └── RMG.txt
│       │       ├── Super Mario Galaxy 2
│       │       │   ├── metadata.json
│       │       │   └── SB4.txt
│       │       ├── Super Mario Sunshine
│       │       │   ├── GMS.txt
│       │       │   └── metadata.json
│       │       ├── Takt of Magic
│       │       │   ├── metadata.json
│       │       │   └── ROS.txt
│       │       ├── The Conduit
│       │       │   ├── metadata.json
│       │       │   └── RCJ.txt
│       │       ├── The House of the Dead Overkill
│       │       │   ├── metadata.json
│       │       │   └── RHO.txt
│       │       ├── The Last Story
│       │       │   ├── metadata.json
│       │       │   └── SLS.txt
│       │       ├── The Legend of Zelda Twilight Princess GC
│       │       │   ├── GZ2.txt
│       │       │   └── metadata.json
│       │       ├── The Legend of Zelda Twilight Princess Wii
│       │       │   ├── metadata.json
│       │       │   └── RZD.txt
│       │       ├── Wii Play
│       │       │   ├── metadata.json
│       │       │   └── RHA.txt
│       │       ├── Xenoblade Chronicles
│       │       │   ├── metadata.json
│       │       │   └── SX4.txt
│       │       └── Zangeki no Reginleiv
│       │           ├── metadata.json
│       │           └── RZN.txt
│       ├── Profiles
│       │   ├── GCPad
│       │   │   └── SDL Gamepad.ini
│       │   └── Wiimote
│       │       └── Wii Remote with MotionPlus Pointing.ini
│       ├── Resources
│       │   ├── achievements_game.png
│       │   ├── achievements_locked.png
│       │   ├── achievements_player.png
│       │   ├── achievements_unlocked.png
│       │   ├── dolphin_logo@2x.png
│       │   ├── dolphin_logo.png
│       │   ├── Flag_Australia@2x.png
│       │   ├── Flag_Australia@4x.png
│       │   ├── Flag_Australia.png
│       │   ├── Flag_Europe@2x.png
│       │   ├── Flag_Europe@4x.png
│       │   ├── Flag_Europe.png
│       │   ├── Flag_France@2x.png
│       │   ├── Flag_France@4x.png
│       │   ├── Flag_France.png
│       │   ├── Flag_Germany@2x.png
│       │   ├── Flag_Germany@4x.png
│       │   ├── Flag_Germany.png
│       │   ├── Flag_International@2x.png
│       │   ├── Flag_International@4x.png
│       │   ├── Flag_International.png
│       │   ├── Flag_Italy@2x.png
│       │   ├── Flag_Italy@4x.png
│       │   ├── Flag_Italy.png
│       │   ├── Flag_Japan@2x.png
│       │   ├── Flag_Japan@4x.png
│       │   ├── Flag_Japan.png
│       │   ├── Flag_Korea@2x.png
│       │   ├── Flag_Korea@4x.png
│       │   ├── Flag_Korea.png
│       │   ├── Flag_Netherlands@2x.png
│       │   ├── Flag_Netherlands@4x.png
│       │   ├── Flag_Netherlands.png
│       │   ├── Flag_Russia@2x.png
│       │   ├── Flag_Russia@4x.png
│       │   ├── Flag_Russia.png
│       │   ├── Flag_Spain@2x.png
│       │   ├── Flag_Spain@4x.png
│       │   ├── Flag_Spain.png
│       │   ├── Flag_Taiwan@2x.png
│       │   ├── Flag_Taiwan@4x.png
│       │   ├── Flag_Taiwan.png
│       │   ├── Flag_Unknown@2x.png
│       │   ├── Flag_Unknown@4x.png
│       │   ├── Flag_Unknown.png
│       │   ├── Flag_USA@2x.png
│       │   ├── Flag_USA@4x.png
│       │   ├── Flag_USA.png
│       │   ├── isoproperties_disc.png
│       │   ├── isoproperties_file.png
│       │   ├── isoproperties_folder.png
│       │   ├── nobanner@2x.png
│       │   ├── nobanner@4x.png
│       │   ├── nobanner.png
│       │   ├── OSD_Font.ttf
│       │   ├── OSD_Font_VeraMono_Copyright.txt
│       │   ├── Platform_File@2x.png
│       │   ├── Platform_File@4x.png
│       │   ├── Platform_File.png
│       │   ├── Platform_Gamecube@2x.png
│       │   ├── Platform_Gamecube@4x.png
│       │   ├── Platform_Gamecube.png
│       │   ├── Platform_Triforce@2x.png
│       │   ├── Platform_Triforce@4x.png
│       │   ├── Platform_Triforce.png
│       │   ├── Platform_Wad@2x.png
│       │   ├── Platform_Wad@4x.png
│       │   ├── Platform_Wad.png
│       │   ├── Platform_Wii@2x.png
│       │   ├── Platform_Wii@4x.png
│       │   └── Platform_Wii.png
│       ├── Shaders
│       │   ├── 16bit.glsl
│       │   ├── 32bit.glsl
│       │   ├── acidmetal.glsl
│       │   ├── acidtrip2.glsl
│       │   ├── acidtrip.glsl
│       │   ├── Anaglyph
│       │   │   ├── dubois.glsl
│       │   │   ├── dubois-LCD-Amber-Blue.glsl
│       │   │   ├── dubois-LCD-Green-Magenta.glsl
│       │   │   ├── fullcolor.glsl
│       │   │   ├── grayscale2.glsl
│       │   │   └── grayscale.glsl
│       │   ├── asciiart.glsl
│       │   ├── AutoHDR.glsl
│       │   ├── auto_toon2.glsl
│       │   ├── auto_toon.glsl
│       │   ├── bad_bloom.glsl
│       │   ├── brighten.glsl
│       │   ├── chrismas.glsl
│       │   ├── cool1.glsl
│       │   ├── darkerbrighter.glsl
│       │   ├── default_pre_post_process.glsl
│       │   ├── emboss.glsl
│       │   ├── fire2.glsl
│       │   ├── fire.glsl
│       │   ├── firewater.glsl
│       │   ├── FXAA.glsl
│       │   ├── grayscale2.glsl
│       │   ├── grayscale.glsl
│       │   ├── integer_scaling.glsl
│       │   ├── invert_blue.glsl
│       │   ├── invertedoutline.glsl
│       │   ├── invert.glsl
│       │   ├── lens_distortion.glsl
│       │   ├── mad_world.glsl
│       │   ├── nightvision2.glsl
│       │   ├── nightvision2scanlines.glsl
│       │   ├── nightvision.glsl
│       │   ├── Passive
│       │   │   └── horizontal.glsl
│       │   ├── PerceptualHDR.glsl
│       │   ├── posterize2.glsl
│       │   ├── posterize.glsl
│       │   ├── primarycolors.glsl
│       │   ├── sepia.glsl
│       │   ├── sketchy.glsl
│       │   ├── spookey1.glsl
│       │   ├── spookey2.glsl
│       │   ├── sunset.glsl
│       │   ├── swap_RGB_BGR.glsl
│       │   ├── swap_RGB_BRG.glsl
│       │   ├── swap_RGB_GBR.glsl
│       │   ├── swap_RGB_GRB.glsl
│       │   ├── swap_RGB_RBG.glsl
│       │   └── toxic.glsl
│       ├── Themes
│       │   ├── Clean
│       │   │   ├── assembler_assemble@2x.png
│       │   │   ├── assembler_assemble@4x.png
│       │   │   ├── assembler_assemble.png
│       │   │   ├── assembler_clipboard.png
│       │   │   ├── assembler_inject@2x.png
│       │   │   ├── assembler_inject@4x.png
│       │   │   ├── assembler_inject.png
│       │   │   ├── assembler_new@2x.png
│       │   │   ├── assembler_new@4x.png
│       │   │   ├── assembler_new.png
│       │   │   ├── assembler_openasm@2x.png
│       │   │   ├── assembler_openasm@4x.png
│       │   │   ├── assembler_openasm.png
│       │   │   ├── assembler_save@2x.png
│       │   │   ├── assembler_save@4x.png
│       │   │   ├── assembler_save.png
│       │   │   ├── browse@2x.png
│       │   │   ├── browse@4x.png
│       │   │   ├── browse.png
│       │   │   ├── classic@2x.png
│       │   │   ├── classic@4x.png
│       │   │   ├── classic.png
│       │   │   ├── config@2x.png
│       │   │   ├── config@4x.png
│       │   │   ├── config.png
│       │   │   ├── debugger_add_breakpoint@2x.png
│       │   │   ├── debugger_add_breakpoint@4x.png
│       │   │   ├── debugger_add_breakpoint.png
│       │   │   ├── debugger_add_memorycheck@2x.png
│       │   │   ├── debugger_add_memorycheck@4x.png
│       │   │   ├── debugger_add_memorycheck.png
│       │   │   ├── debugger_breakpoint@2x.png
│       │   │   ├── debugger_breakpoint@4x.png
│       │   │   ├── debugger_breakpoint.png
│       │   │   ├── debugger_clear@2x.png
│       │   │   ├── debugger_clear@4x.png
│       │   │   ├── debugger_clear.png
│       │   │   ├── debugger_delete@2x.png
│       │   │   ├── debugger_delete@4x.png
│       │   │   ├── debugger_delete.png
│       │   │   ├── debugger_load@2x.png
│       │   │   ├── debugger_load@4x.png
│       │   │   ├── debugger_load.png
│       │   │   ├── debugger_save@2x.png
│       │   │   ├── debugger_save@4x.png
│       │   │   ├── debugger_save.png
│       │   │   ├── debugger_set_pc@2x.png
│       │   │   ├── debugger_set_pc@4x.png
│       │   │   ├── debugger_set_pc.png
│       │   │   ├── debugger_show_pc@2x.png
│       │   │   ├── debugger_show_pc@4x.png
│       │   │   ├── debugger_show_pc.png
│       │   │   ├── debugger_skip@2x.png
│       │   │   ├── debugger_skip@4x.png
│       │   │   ├── debugger_skip.png
│       │   │   ├── debugger_step_in@2x.png
│       │   │   ├── debugger_step_in@4x.png
│       │   │   ├── debugger_step_in.png
│       │   │   ├── debugger_step_out@2x.png
│       │   │   ├── debugger_step_out@4x.png
│       │   │   ├── debugger_step_out.png
│       │   │   ├── debugger_step_over@2x.png
│       │   │   ├── debugger_step_over@4x.png
│       │   │   ├── debugger_step_over.png
│       │   │   ├── fullscreen@2x.png
│       │   │   ├── fullscreen@4x.png
│       │   │   ├── fullscreen.png
│       │   │   ├── gcpad@2x.png
│       │   │   ├── gcpad@4x.png
│       │   │   ├── gcpad.png
│       │   │   ├── graphics@2x.png
│       │   │   ├── graphics@4x.png
│       │   │   ├── graphics.png
│       │   │   ├── open@2x.png
│       │   │   ├── open@4x.png
│       │   │   ├── open.png
│       │   │   ├── pause@2x.png
│       │   │   ├── pause@4x.png
│       │   │   ├── pause.png
│       │   │   ├── play@2x.png
│       │   │   ├── play@4x.png
│       │   │   ├── play.png
│       │   │   ├── refresh@2x.png
│       │   │   ├── refresh@4x.png
│       │   │   ├── refresh.png
│       │   │   ├── screenshot@2x.png
│       │   │   ├── screenshot@4x.png
│       │   │   ├── screenshot.png
│       │   │   ├── stop@2x.png
│       │   │   ├── stop@4x.png
│       │   │   ├── stop.png
│       │   │   ├── wiimote@2x.png
│       │   │   ├── wiimote@4x.png
│       │   │   └── wiimote.png
│       │   ├── Clean Blue
│       │   │   ├── assembler_assemble@2x.png
│       │   │   ├── assembler_assemble@4x.png
│       │   │   ├── assembler_assemble.png
│       │   │   ├── assembler_clipboard.png
│       │   │   ├── assembler_inject@2x.png
│       │   │   ├── assembler_inject@4x.png
│       │   │   ├── assembler_inject.png
│       │   │   ├── assembler_new@2x.png
│       │   │   ├── assembler_new@4x.png
│       │   │   ├── assembler_new.png
│       │   │   ├── assembler_openasm@2x.png
│       │   │   ├── assembler_openasm@4x.png
│       │   │   ├── assembler_openasm.png
│       │   │   ├── assembler_save@2x.png
│       │   │   ├── assembler_save@4x.png
│       │   │   ├── assembler_save.png
│       │   │   ├── browse@2x.png
│       │   │   ├── browse@4x.png
│       │   │   ├── browse.png
│       │   │   ├── classic@2x.png
│       │   │   ├── classic@4x.png
│       │   │   ├── classic.png
│       │   │   ├── config@2x.png
│       │   │   ├── config@4x.png
│       │   │   ├── config.png
│       │   │   ├── debugger_add_breakpoint@2x.png
│       │   │   ├── debugger_add_breakpoint@4x.png
│       │   │   ├── debugger_add_breakpoint.png
│       │   │   ├── debugger_add_memorycheck@2x.png
│       │   │   ├── debugger_add_memorycheck@4x.png
│       │   │   ├── debugger_add_memorycheck.png
│       │   │   ├── debugger_breakpoint@2x.png
│       │   │   ├── debugger_breakpoint@4x.png
│       │   │   ├── debugger_breakpoint.png
│       │   │   ├── debugger_clear@2x.png
│       │   │   ├── debugger_clear@4x.png
│       │   │   ├── debugger_clear.png
│       │   │   ├── debugger_delete@2x.png
│       │   │   ├── debugger_delete@4x.png
│       │   │   ├── debugger_delete.png
│       │   │   ├── debugger_load@2x.png
│       │   │   ├── debugger_load@4x.png
│       │   │   ├── debugger_load.png
│       │   │   ├── debugger_save@2x.png
│       │   │   ├── debugger_save@4x.png
│       │   │   ├── debugger_save.png
│       │   │   ├── debugger_set_pc@2x.png
│       │   │   ├── debugger_set_pc@4x.png
│       │   │   ├── debugger_set_pc.png
│       │   │   ├── debugger_show_pc@2x.png
│       │   │   ├── debugger_show_pc@4x.png
│       │   │   ├── debugger_show_pc.png
│       │   │   ├── debugger_skip@2x.png
│       │   │   ├── debugger_skip@4x.png
│       │   │   ├── debugger_skip.png
│       │   │   ├── debugger_step_in@2x.png
│       │   │   ├── debugger_step_in@4x.png
│       │   │   ├── debugger_step_in.png
│       │   │   ├── debugger_step_out@2x.png
│       │   │   ├── debugger_step_out@4x.png
│       │   │   ├── debugger_step_out.png
│       │   │   ├── debugger_step_over@2x.png
│       │   │   ├── debugger_step_over@4x.png
│       │   │   ├── debugger_step_over.png
│       │   │   ├── fullscreen@2x.png
│       │   │   ├── fullscreen@4x.png
│       │   │   ├── fullscreen.png
│       │   │   ├── gcpad@2x.png
│       │   │   ├── gcpad@4x.png
│       │   │   ├── gcpad.png
│       │   │   ├── graphics@2x.png
│       │   │   ├── graphics@4x.png
│       │   │   ├── graphics.png
│       │   │   ├── open@2x.png
│       │   │   ├── open@4x.png
│       │   │   ├── open.png
│       │   │   ├── pause@2x.png
│       │   │   ├── pause@4x.png
│       │   │   ├── pause.png
│       │   │   ├── play@2x.png
│       │   │   ├── play@4x.png
│       │   │   ├── play.png
│       │   │   ├── refresh@2x.png
│       │   │   ├── refresh@4x.png
│       │   │   ├── refresh.png
│       │   │   ├── screenshot@2x.png
│       │   │   ├── screenshot@4x.png
│       │   │   ├── screenshot.png
│       │   │   ├── stop@2x.png
│       │   │   ├── stop@4x.png
│       │   │   ├── stop.png
│       │   │   ├── wiimote@2x.png
│       │   │   ├── wiimote@4x.png
│       │   │   └── wiimote.png
│       │   ├── Clean Emerald
│       │   │   ├── assembler_assemble@2x.png
│       │   │   ├── assembler_assemble@4x.png
│       │   │   ├── assembler_assemble.png
│       │   │   ├── assembler_clipboard.png
│       │   │   ├── assembler_inject@2x.png
│       │   │   ├── assembler_inject@4x.png
│       │   │   ├── assembler_inject.png
│       │   │   ├── assembler_new@2x.png
│       │   │   ├── assembler_new@4x.png
│       │   │   ├── assembler_new.png
│       │   │   ├── assembler_openasm@2x.png
│       │   │   ├── assembler_openasm@4x.png
│       │   │   ├── assembler_openasm.png
│       │   │   ├── assembler_save@2x.png
│       │   │   ├── assembler_save@4x.png
│       │   │   ├── assembler_save.png
│       │   │   ├── browse@2x.png
│       │   │   ├── browse@4x.png
│       │   │   ├── browse.png
│       │   │   ├── classic@2x.png
│       │   │   ├── classic@4x.png
│       │   │   ├── classic.png
│       │   │   ├── config@2x.png
│       │   │   ├── config@4x.png
│       │   │   ├── config.png
│       │   │   ├── debugger_add_breakpoint@2x.png
│       │   │   ├── debugger_add_breakpoint@4x.png
│       │   │   ├── debugger_add_breakpoint.png
│       │   │   ├── debugger_add_memorycheck@2x.png
│       │   │   ├── debugger_add_memorycheck@4x.png
│       │   │   ├── debugger_add_memorycheck.png
│       │   │   ├── debugger_breakpoint@2x.png
│       │   │   ├── debugger_breakpoint@4x.png
│       │   │   ├── debugger_breakpoint.png
│       │   │   ├── debugger_clear@2x.png
│       │   │   ├── debugger_clear@4x.png
│       │   │   ├── debugger_clear.png
│       │   │   ├── debugger_delete@2x.png
│       │   │   ├── debugger_delete@4x.png
│       │   │   ├── debugger_delete.png
│       │   │   ├── debugger_load@2x.png
│       │   │   ├── debugger_load@4x.png
│       │   │   ├── debugger_load.png
│       │   │   ├── debugger_save@2x.png
│       │   │   ├── debugger_save@4x.png
│       │   │   ├── debugger_save.png
│       │   │   ├── debugger_set_pc@2x.png
│       │   │   ├── debugger_set_pc@4x.png
│       │   │   ├── debugger_set_pc.png
│       │   │   ├── debugger_show_pc@2x.png
│       │   │   ├── debugger_show_pc@4x.png
│       │   │   ├── debugger_show_pc.png
│       │   │   ├── debugger_skip@2x.png
│       │   │   ├── debugger_skip@4x.png
│       │   │   ├── debugger_skip.png
│       │   │   ├── debugger_step_in@2x.png
│       │   │   ├── debugger_step_in@4x.png
│       │   │   ├── debugger_step_in.png
│       │   │   ├── debugger_step_out@2x.png
│       │   │   ├── debugger_step_out@4x.png
│       │   │   ├── debugger_step_out.png
│       │   │   ├── debugger_step_over@2x.png
│       │   │   ├── debugger_step_over@4x.png
│       │   │   ├── debugger_step_over.png
│       │   │   ├── fullscreen@2x.png
│       │   │   ├── fullscreen@4x.png
│       │   │   ├── fullscreen.png
│       │   │   ├── gcpad@2x.png
│       │   │   ├── gcpad@4x.png
│       │   │   ├── gcpad.png
│       │   │   ├── graphics@2x.png
│       │   │   ├── graphics@4x.png
│       │   │   ├── graphics.png
│       │   │   ├── open@2x.png
│       │   │   ├── open@4x.png
│       │   │   ├── open.png
│       │   │   ├── pause@2x.png
│       │   │   ├── pause@4x.png
│       │   │   ├── pause.png
│       │   │   ├── play@2x.png
│       │   │   ├── play@4x.png
│       │   │   ├── play.png
│       │   │   ├── refresh@2x.png
│       │   │   ├── refresh@4x.png
│       │   │   ├── refresh.png
│       │   │   ├── screenshot@2x.png
│       │   │   ├── screenshot@4x.png
│       │   │   ├── screenshot.png
│       │   │   ├── stop@2x.png
│       │   │   ├── stop@4x.png
│       │   │   ├── stop.png
│       │   │   ├── wiimote@2x.png
│       │   │   ├── wiimote@4x.png
│       │   │   └── wiimote.png
│       │   ├── Clean Lite
│       │   │   ├── assembler_assemble@2x.png
│       │   │   ├── assembler_assemble@4x.png
│       │   │   ├── assembler_assemble.png
│       │   │   ├── assembler_clipboard.png
│       │   │   ├── assembler_inject@2x.png
│       │   │   ├── assembler_inject@4x.png
│       │   │   ├── assembler_inject.png
│       │   │   ├── assembler_new@2x.png
│       │   │   ├── assembler_new@4x.png
│       │   │   ├── assembler_new.png
│       │   │   ├── assembler_openasm@2x.png
│       │   │   ├── assembler_openasm@4x.png
│       │   │   ├── assembler_openasm.png
│       │   │   ├── assembler_save@2x.png
│       │   │   ├── assembler_save@4x.png
│       │   │   ├── assembler_save.png
│       │   │   ├── browse@2x.png
│       │   │   ├── browse@4x.png
│       │   │   ├── browse.png
│       │   │   ├── classic@2x.png
│       │   │   ├── classic@4x.png
│       │   │   ├── classic.png
│       │   │   ├── config@2x.png
│       │   │   ├── config@4x.png
│       │   │   ├── config.png
│       │   │   ├── debugger_add_breakpoint@2x.png
│       │   │   ├── debugger_add_breakpoint@4x.png
│       │   │   ├── debugger_add_breakpoint.png
│       │   │   ├── debugger_add_memorycheck@2x.png
│       │   │   ├── debugger_add_memorycheck@4x.png
│       │   │   ├── debugger_add_memorycheck.png
│       │   │   ├── debugger_breakpoint@2x.png
│       │   │   ├── debugger_breakpoint@4x.png
│       │   │   ├── debugger_breakpoint.png
│       │   │   ├── debugger_clear@2x.png
│       │   │   ├── debugger_clear@4x.png
│       │   │   ├── debugger_clear.png
│       │   │   ├── debugger_delete@2x.png
│       │   │   ├── debugger_delete@4x.png
│       │   │   ├── debugger_delete.png
│       │   │   ├── debugger_load@2x.png
│       │   │   ├── debugger_load@4x.png
│       │   │   ├── debugger_load.png
│       │   │   ├── debugger_save@2x.png
│       │   │   ├── debugger_save@4x.png
│       │   │   ├── debugger_save.png
│       │   │   ├── debugger_set_pc@2x.png
│       │   │   ├── debugger_set_pc@4x.png
│       │   │   ├── debugger_set_pc.png
│       │   │   ├── debugger_show_pc@2x.png
│       │   │   ├── debugger_show_pc@4x.png
│       │   │   ├── debugger_show_pc.png
│       │   │   ├── debugger_skip@2x.png
│       │   │   ├── debugger_skip@4x.png
│       │   │   ├── debugger_skip.png
│       │   │   ├── debugger_step_in@2x.png
│       │   │   ├── debugger_step_in@4x.png
│       │   │   ├── debugger_step_in.png
│       │   │   ├── debugger_step_out@2x.png
│       │   │   ├── debugger_step_out@4x.png
│       │   │   ├── debugger_step_out.png
│       │   │   ├── debugger_step_over@2x.png
│       │   │   ├── debugger_step_over@4x.png
│       │   │   ├── debugger_step_over.png
│       │   │   ├── fullscreen@2x.png
│       │   │   ├── fullscreen@4x.png
│       │   │   ├── fullscreen.png
│       │   │   ├── gcpad@2x.png
│       │   │   ├── gcpad@4x.png
│       │   │   ├── gcpad.png
│       │   │   ├── graphics@2x.png
│       │   │   ├── graphics@4x.png
│       │   │   ├── graphics.png
│       │   │   ├── open@2x.png
│       │   │   ├── open@4x.png
│       │   │   ├── open.png
│       │   │   ├── pause@2x.png
│       │   │   ├── pause@4x.png
│       │   │   ├── pause.png
│       │   │   ├── play@2x.png
│       │   │   ├── play@4x.png
│       │   │   ├── play.png
│       │   │   ├── refresh@2x.png
│       │   │   ├── refresh@4x.png
│       │   │   ├── refresh.png
│       │   │   ├── screenshot@2x.png
│       │   │   ├── screenshot@4x.png
│       │   │   ├── screenshot.png
│       │   │   ├── stop@2x.png
│       │   │   ├── stop@4x.png
│       │   │   ├── stop.png
│       │   │   ├── wiimote@2x.png
│       │   │   ├── wiimote@4x.png
│       │   │   └── wiimote.png
│       │   └── Clean Pink
│       │       ├── assembler_assemble@2x.png
│       │       ├── assembler_assemble@4x.png
│       │       ├── assembler_assemble.png
│       │       ├── assembler_clipboard.png
│       │       ├── assembler_inject@2x.png
│       │       ├── assembler_inject@4x.png
│       │       ├── assembler_inject.png
│       │       ├── assembler_new@2x.png
│       │       ├── assembler_new@4x.png
│       │       ├── assembler_new.png
│       │       ├── assembler_openasm@2x.png
│       │       ├── assembler_openasm@4x.png
│       │       ├── assembler_openasm.png
│       │       ├── assembler_save@2x.png
│       │       ├── assembler_save@4x.png
│       │       ├── assembler_save.png
│       │       ├── browse@2x.png
│       │       ├── browse@4x.png
│       │       ├── browse.png
│       │       ├── classic@2x.png
│       │       ├── classic@4x.png
│       │       ├── classic.png
│       │       ├── config@2x.png
│       │       ├── config@4x.png
│       │       ├── config.png
│       │       ├── debugger_add_breakpoint@2x.png
│       │       ├── debugger_add_breakpoint@4x.png
│       │       ├── debugger_add_breakpoint.png
│       │       ├── debugger_add_memorycheck@2x.png
│       │       ├── debugger_add_memorycheck@4x.png
│       │       ├── debugger_add_memorycheck.png
│       │       ├── debugger_breakpoint@2x.png
│       │       ├── debugger_breakpoint@4x.png
│       │       ├── debugger_breakpoint.png
│       │       ├── debugger_clear@2x.png
│       │       ├── debugger_clear@4x.png
│       │       ├── debugger_clear.png
│       │       ├── debugger_delete@2x.png
│       │       ├── debugger_delete@4x.png
│       │       ├── debugger_delete.png
│       │       ├── debugger_load@2x.png
│       │       ├── debugger_load@4x.png
│       │       ├── debugger_load.png
│       │       ├── debugger_save@2x.png
│       │       ├── debugger_save@4x.png
│       │       ├── debugger_save.png
│       │       ├── debugger_set_pc@2x.png
│       │       ├── debugger_set_pc@4x.png
│       │       ├── debugger_set_pc.png
│       │       ├── debugger_show_pc@2x.png
│       │       ├── debugger_show_pc@4x.png
│       │       ├── debugger_show_pc.png
│       │       ├── debugger_skip@2x.png
│       │       ├── debugger_skip@4x.png
│       │       ├── debugger_skip.png
│       │       ├── debugger_step_in@2x.png
│       │       ├── debugger_step_in@4x.png
│       │       ├── debugger_step_in.png
│       │       ├── debugger_step_out@2x.png
│       │       ├── debugger_step_out@4x.png
│       │       ├── debugger_step_out.png
│       │       ├── debugger_step_over@2x.png
│       │       ├── debugger_step_over@4x.png
│       │       ├── debugger_step_over.png
│       │       ├── fullscreen@2x.png
│       │       ├── fullscreen@4x.png
│       │       ├── fullscreen.png
│       │       ├── gcpad@2x.png
│       │       ├── gcpad@4x.png
│       │       ├── gcpad.png
│       │       ├── graphics@2x.png
│       │       ├── graphics@4x.png
│       │       ├── graphics.png
│       │       ├── open@2x.png
│       │       ├── open@4x.png
│       │       ├── open.png
│       │       ├── pause@2x.png
│       │       ├── pause@4x.png
│       │       ├── pause.png
│       │       ├── play@2x.png
│       │       ├── play@4x.png
│       │       ├── play.png
│       │       ├── refresh@2x.png
│       │       ├── refresh@4x.png
│       │       ├── refresh.png
│       │       ├── screenshot@2x.png
│       │       ├── screenshot@4x.png
│       │       ├── screenshot.png
│       │       ├── stop@2x.png
│       │       ├── stop@4x.png
│       │       ├── stop.png
│       │       ├── wiimote@2x.png
│       │       ├── wiimote@4x.png
│       │       └── wiimote.png
│       ├── totaldb.dsy
│       ├── Triforce
│       │   └── segaboot.gcm
│       ├── triforcetdb-en.txt
│       ├── Wii
│       │   └── shared2
│       │       └── wc24
│       │           ├── mbox
│       │           │   ├── Readme.txt
│       │           │   ├── wc24recv.ctl
│       │           │   ├── wc24recv.mbx
│       │           │   ├── wc24send.ctl
│       │           │   └── wc24send.mbx
│       │           ├── misc.bin
│       │           ├── nwc24dl.bin
│       │           ├── nwc24fl.bin
│       │           ├── nwc24fls.bin
│       │           ├── nwc24msg.cbk
│       │           └── nwc24msg.cfg
│       ├── wiitdb-de.txt
│       ├── wiitdb-en.txt
│       ├── wiitdb-es.txt
│       ├── wiitdb-fr.txt
│       ├── wiitdb-it.txt
│       ├── wiitdb-ja.txt
│       ├── wiitdb-ko.txt
│       ├── wiitdb-nl.txt
│       ├── wiitdb-pt.txt
│       ├── wiitdb-ru.txt
│       ├── wiitdb-zh_CN.txt
│       └── wiitdb-zh_TW.txt
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
├── fuse
│   ├── 128-0.rom
│   ├── 128-1.rom
│   ├── 128p-0.rom
│   ├── 128p-1.rom
│   ├── 256s-0.rom
│   ├── 256s-1.rom
│   ├── 256s-2.rom
│   ├── 256s-3.rom
│   ├── gluck.rom
│   └── trdos.rom
├── gba_bios.bin
├── gb_bios.bin
├── gbc_bios.bin
├── gexpress.pce
├── hatari
│   └── tos
│       └── tos.img
├── jaguarcd
│   ├── [BIOS] Atari Jaguar CD (World).j64
│   └── [BIOS] Atari Jaguar Developer CD (World).j64
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
│   │   ├── autofire
│   │   │   ├── autofire_menu.lua
│   │   │   ├── autofire_save.lua
│   │   │   ├── init.lua
│   │   │   └── plugin.json
│   │   ├── boot.lua
│   │   ├── cheat
│   │   │   ├── cheat_json.lua
│   │   │   ├── cheat_simple.lua
│   │   │   ├── cheat_xml.lua
│   │   │   ├── init.lua
│   │   │   ├── plugin.json
│   │   │   └── xml_to_json.lua
│   │   ├── cheatfind
│   │   │   ├── init.lua
│   │   │   └── plugin.json
│   │   ├── commonui
│   │   │   ├── init.lua
│   │   │   └── plugin.json
│   │   ├── console
│   │   │   ├── init.lua
│   │   │   └── plugin.json
│   │   ├── data
│   │   │   ├── button_char.lua
│   │   │   ├── database.lua
│   │   │   ├── data_command.lua
│   │   │   ├── data_gameinit.lua
│   │   │   ├── data_hiscore.lua
│   │   │   ├── data_history.lua
│   │   │   ├── data_mameinfo.lua
│   │   │   ├── data_marp.lua
│   │   │   ├── data_messinfo.lua
│   │   │   ├── data_story.lua
│   │   │   ├── data_sysinfo.lua
│   │   │   ├── init.lua
│   │   │   ├── load_dat.lua
│   │   │   └── plugin.json
│   │   ├── discord
│   │   │   ├── init.lua
│   │   │   └── plugin.json
│   │   ├── dummy
│   │   │   ├── init.lua
│   │   │   └── plugin.json
│   │   ├── gdbstub
│   │   │   ├── init.lua
│   │   │   └── plugin.json
│   │   ├── hiscore
│   │   │   ├── hiscore.dat
│   │   │   ├── init.lua
│   │   │   ├── plugin.json
│   │   │   └── sort_hiscore.lua
│   │   ├── inputmacro
│   │   │   ├── init.lua
│   │   │   ├── inputmacro_menu.lua
│   │   │   ├── inputmacro_persist.lua
│   │   │   └── plugin.json
│   │   ├── json
│   │   │   ├── init.lua
│   │   │   ├── LICENSE
│   │   │   ├── plugin.json
│   │   │   └── README.md
│   │   ├── layout
│   │   │   ├── init.lua
│   │   │   └── plugin.json
│   │   ├── offscreenreload
│   │   │   ├── init.lua
│   │   │   ├── offscreenreload_menu.lua
│   │   │   ├── offscreenreload_persist.lua
│   │   │   └── plugin.json
│   │   ├── plugin.schema
│   │   ├── portname
│   │   │   ├── init.lua
│   │   │   └── plugin.json
│   │   ├── README.md
│   │   ├── timecode
│   │   │   ├── init.lua
│   │   │   └── plugin.json
│   │   ├── timer
│   │   │   ├── init.lua
│   │   │   ├── plugin.json
│   │   │   └── timer_persist.lua
│   │   ├── vector
│   │   │   ├── init.lua
│   │   │   └── plugin.json
│   │   └── xml
│   │       ├── init.lua
│   │       ├── LICENSE.txt
│   │       └── plugin.json
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
├── Mupen64plus
│   └── IPL.n64
├── neocd
│   ├── neocd.srm
│   ├── neocd_z.rom
│   └── uni-bioscd.rom
├── panafz10.bin
├── pcsx2
│   └── bios
│       ├── SCPH-70004_BIOS_V12_PAL_200.BIN
│       ├── SCPH-70004_BIOS_V12_PAL_200.EROM
│       ├── SCPH-70004_BIOS_V12_PAL_200.MEC
│       ├── SCPH-70004_BIOS_V12_PAL_200.NVM
│       ├── SCPH-70004_BIOS_V12_PAL_200.ROM1
│       ├── SCPH-70004_BIOS_V12_PAL_200.ROM2
│       ├── SCPH-70012_BIOS_V12_USA_200.bin
│       ├── SCPH-70012_BIOS_V12_USA_200.MEC
│       └── SCPH-70012_BIOS_V12_USA_200.NVM
├── PPSSPP
│   ├── adhoc-servers.json
│   ├── asciifont_atlas.meta
│   ├── asciifont_atlas.zim
│   ├── cheats.json
│   ├── compat.ini
│   ├── compatvr.ini
│   ├── debugger
│   │   ├── asset-manifest.json
│   │   ├── favicon.ico
│   │   ├── index.html
│   │   ├── manifest.json
│   │   └── static
│   │       ├── css
│   │       │   ├── main.3eab8a01.css
│   │       │   └── main.3eab8a01.css.map
│   │       ├── js
│   │       │   ├── main.fe87e942.js
│   │       │   ├── main.fe87e942.js.LICENSE.txt
│   │       │   └── main.fe87e942.js.map
│   │       └── media
│   │           └── logo.94f885ce93dfb6d29a122402a15cccca.svg
│   ├── flash0
│   │   └── font
│   │       ├── jpn0.pgf
│   │       ├── kr0.pgf
│   │       ├── ltn0.pgf
│   │       ├── ltn10.pgf
│   │       ├── ltn11.pgf
│   │       ├── ltn12.pgf
│   │       ├── ltn13.pgf
│   │       ├── ltn14.pgf
│   │       ├── ltn15.pgf
│   │       ├── ltn1.pgf
│   │       ├── ltn2.pgf
│   │       ├── ltn3.pgf
│   │       ├── ltn4.pgf
│   │       ├── ltn5.pgf
│   │       ├── ltn6.pgf
│   │       ├── ltn7.pgf
│   │       ├── ltn8.pgf
│   │       └── ltn9.pgf
│   ├── font_atlas.meta
│   ├── font_atlas.zim
│   ├── gamecontrollerdb.txt
│   ├── Inconsolata-Regular.ttf
│   ├── infra-dns.json
│   ├── knownfuncs.ini
│   ├── lang
│   │   ├── ar_AE.ini
│   │   ├── az_AZ.ini
│   │   ├── be_BY.ini
│   │   ├── bg_BG.ini
│   │   ├── ca_ES.ini
│   │   ├── cz_CZ.ini
│   │   ├── da_DK.ini
│   │   ├── de_DE.ini
│   │   ├── dr_ID.ini
│   │   ├── en_US.ini
│   │   ├── es_ES.ini
│   │   ├── es_LA.ini
│   │   ├── fa_IR.ini
│   │   ├── fi_FI.ini
│   │   ├── fr_FR.ini
│   │   ├── gl_ES.ini
│   │   ├── gr_EL.ini
│   │   ├── he_IL.ini
│   │   ├── he_IL_invert.ini
│   │   ├── hr_HR.ini
│   │   ├── hu_HU.ini
│   │   ├── id_ID.ini
│   │   ├── it_IT.ini
│   │   ├── ja_JP.ini
│   │   ├── jv_ID.ini
│   │   ├── km_KH.ini
│   │   ├── ko_KR.ini
│   │   ├── ku_SO.ini
│   │   ├── lo_LA.ini
│   │   ├── lt-LT.ini
│   │   ├── ms_MY.ini
│   │   ├── nl_NL.ini
│   │   ├── nn_NO.ini
│   │   ├── no_NO.ini
│   │   ├── pl_PL.ini
│   │   ├── pt_BR.ini
│   │   ├── pt_PT.ini
│   │   ├── README.md
│   │   ├── ro_RO.ini
│   │   ├── ru_RU.ini
│   │   ├── sv_SE.ini
│   │   ├── tg_PH.ini
│   │   ├── th_TH.ini
│   │   ├── tr_TR.ini
│   │   ├── uk_UA.ini
│   │   ├── vi_VN.ini
│   │   ├── zh_CN.ini
│   │   └── zh_TW.ini
│   ├── langregion.ini
│   ├── mime
│   │   └── ppsspp.xml
│   ├── ppge_atlas.meta
│   ├── ppge_atlas.zim
│   ├── redump.csv
│   ├── Roboto_Condensed-Bold.ttf
│   ├── Roboto_Condensed-Italic.ttf
│   ├── Roboto_Condensed-Light.ttf
│   ├── Roboto_Condensed-Regular.ttf
│   ├── sfx_achievement_unlocked.wav
│   ├── sfx_back.wav
│   ├── sfx_confirm.wav
│   ├── sfx_leaderbord_submitted.wav
│   ├── sfx_select.wav
│   ├── sfx_toggle_off.wav
│   ├── sfx_toggle_on.wav
│   ├── shaders
│   │   ├── 4xhqglsl.fsh
│   │   ├── 4xhqglsl.vsh
│   │   ├── 5xBR.fsh
│   │   ├── 5xBR-lv2.fsh
│   │   ├── 5xBR.vsh
│   │   ├── aacolor.fsh
│   │   ├── aacolor.vsh
│   │   ├── bloom.fsh
│   │   ├── bloomnoblur.fsh
│   │   ├── cartoon.fsh
│   │   ├── cartoon.vsh
│   │   ├── colorcorrection.fsh
│   │   ├── crt.fsh
│   │   ├── defaultshaders.ini
│   │   ├── fakereflections.fsh
│   │   ├── fsr_easu.fsh
│   │   ├── fsr_rcas.fsh
│   │   ├── fxaa.fsh
│   │   ├── fxaa.vsh
│   │   ├── GaussianDownscale.fsh
│   │   ├── naturalA.fsh
│   │   ├── naturalA.vsh
│   │   ├── natural.fsh
│   │   ├── natural.vsh
│   │   ├── persistence.fsh
│   │   ├── psp_color.fsh
│   │   ├── scanlines.fsh
│   │   ├── sharpen.fsh
│   │   ├── smiley_16x16_rgba.bin
│   │   ├── smiley.py
│   │   ├── stereo_red_blue.fsh
│   │   ├── stereo_sbs.fsh
│   │   ├── tex_2xbrz.csh
│   │   ├── tex_4xbrz.csh
│   │   ├── tex_mmpx_adv.csh
│   │   ├── tex_mmpx.csh
│   │   ├── tex_nnedi3_2x_single.csh
│   │   ├── tex_nnedi3_4x_single.csh
│   │   ├── tex_nnedi3_mp_cshift_2x.csh
│   │   ├── tex_nnedi3_mp_cshift_4x.csh
│   │   ├── tex_nnedi3_mp_nns16_pass1_buffer.csh
│   │   ├── tex_nnedi3_mp_nns16_pass1_image.csh
│   │   ├── tex_nnedi3_mp_nns16_pass2.csh
│   │   ├── tex_smiley_2x.csh
│   │   ├── tex_spline36_2x.csh
│   │   ├── tex_spline36_4x.csh
│   │   ├── upscale_bicubic.fsh
│   │   ├── upscale_bicubic.vsh
│   │   ├── upscale_sharp_bilinear.fsh
│   │   ├── upscale_sharp_bilinear.vsh
│   │   ├── upscale_spline36.fsh
│   │   ├── upscale_spline36.vsh
│   │   ├── videoAA.fsh
│   │   └── vignette.fsh
│   ├── themes
│   │   ├── 1995.ini
│   │   ├── alpine.ini
│   │   ├── defaultthemes.ini
│   │   ├── slateforest.ini
│   │   ├── strawberry.ini
│   │   └── vinewood.ini
│   ├── ui_images
│   │   ├── bg.png
│   │   ├── buttons.svg
│   │   ├── drop_shadow.png
│   │   ├── icon_gold.png
│   │   ├── icon.png
│   │   ├── images.svg
│   │   ├── psp_display.png
│   │   ├── retroachievements_logo.png
│   │   ├── stick_line.png
│   │   ├── stick.png
│   │   └── svg_sources.txt
│   ├── upload
│   │   └── index.html
│   └── vfpu
│       ├── vfpu_asin_lut65536.dat
│       ├── vfpu_asin_lut_deltas.dat
│       ├── vfpu_asin_lut_indices.dat
│       ├── vfpu_exp2_lut65536.dat
│       ├── vfpu_exp2_lut.dat
│       ├── vfpu_log2_lut65536.dat
│       ├── vfpu_log2_lut65536_quadratic.dat
│       ├── vfpu_log2_lut.dat
│       ├── vfpu_rcp_lut.dat
│       ├── vfpu_rsqrt_lut.dat
│       ├── vfpu_sin_lut8192.dat
│       ├── vfpu_sin_lut_delta.dat
│       ├── vfpu_sin_lut_exceptions.dat
│       ├── vfpu_sin_lut_interval_delta.dat
│       └── vfpu_sqrt_lut.dat
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
├── stvbios.zip
├── syscard1.pce
├── syscard2.pce
└── syscard3.pce
```