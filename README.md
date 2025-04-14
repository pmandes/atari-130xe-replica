# Atari 130XE (64x4) Assy No. CA200519 motherboard replica

These is a replica of the motherboard of a Atari 130XE 8-bit computer. They were created on the basis of the last version of the board - "CI03579 REV.1 / Assy No. CA200519" - which was mounted in last batches of Atari 65XE, Atari 800XE and Atari 130XE.

It differs from previous versions primarily by using 2/4 memory chips instead of 8 in the Atari 65XE or 16 in the Atari 130XE. It also features a full ECI/CART connector, which was missing in earlier versions of the 65 series. This replica is reproduced almost exactly 1:1 from the original, with only the descriptive layer modified for greater clarity. There may also be other minor improvements, such as the removal of certain errors present in the original.

## The purpose of the project: ##
I created this project mainly out of nostalgia for the 8-bit Atari I had in my childhood, inspired by projects like the Re1200. My intention was not to build a board enhanced with modern modules and extensions, such as the 1088 XEL. I wanted my replica to be as close to the original as possible, with only minor improvements. But above all, it is a substitute onto which you can transplant the original components from your damaged motherboard, which may be rusty, have burnt traces caused by unprofessional repairs, or memory replacements. Your Atari will gain new life with a high-quality motherboard and a great appearance.

![Atari 130 XE motherboard](https://raw.githubusercontent.com/pmandes/atari-130xe-replica/main/images/atari130xe.png)


## Interactive BOM: ##

<p align="center"><a href="https://htmlpreview.github.io/?https://raw.githubusercontent.com/pmandes/atari-130xe-replica/main/bom/ibom.html"><img src="https://raw.githubusercontent.com/pmandes/atari-130xe-replica/main/images/bom.png" height="400"></a></p>

### Major integrated circuits: ###

| No | Chip | Part number | Description |
|--------:|----------------------------|:--------------------:|:------------------|
|  U6     | FREDDIE                    | C061991 (NCR), C061922 (CITE) | Address multiplexer and strobing signal generation for DRAM |
|  U7     | ANTIC                      | C021697 - NTSC, C021698 - PAL | Alpha-Numeric Television Interface Controller |
|  U8     | 6502C SALLY                | C014806 | Main CPU |
|  U17    | GTIA                       | C014805 - NTSC, C014889 - PAL | Graphic Television Interface Adaptor |
|  U22    | POKEY                      | C012294 | Sound generation, serial interface control (SIO), paddle and keyboard support |
|  U23    | PIA                        | C012298, C014795, C014812 | Peripheral Interface Adapter. It supports joystick ports and controls the memory controller |

## Motherboard: ##

<p align="center"><img src="https://raw.githubusercontent.com/pmandes/atari-130xe-replica/main/images/130xe-replica-1.0.jpg" width="480"></a>
<img src="https://raw.githubusercontent.com/pmandes/atari-130xe-replica/main/images/atari-130XE-replica-syscheck.png" width="480"></a></p>

## Changleog: ##

**1.1 (March 2025)**
- corrected minor mistakes in the prototype

**1.0 (August 2023)**
- prototype

## ROMs: ##

- **Atari ROM Checker**, useful tools and a list of all Atari ROMs with checksums: https://www.wudsn.com/productions/atari800/atariromchecker/help/AtariROMChecker.html
- **ROM archive**: http://ftp.pigwa.net/stuff/collections/nir_dary_cds/ROMS/

## Alternative components: ##

- **Atari XE C25953 EMMU Replacement**: https://github.com/mikulski-lab/C25953-emmu
- **Video circuit replacement for the Atari XL/XE**: https://systemembedded.eu/viewtopic.php?t=62
- **Pokeymax 4 by foft**: https://forums.atariage.com/topic/364870-pokeymax-v4-bring-up-thread/

## Useful resources: ##

- **How to upgrade your Atari with Ultimate 1MB, Stereo and Sophia DVI**: https://en.devzine.pl/2019/09/23/how-to-upgrade-your-atari-with-ultimate-1mb-stereo-and-sophia-dvi/
- **Ultra Video XE**: https://arsoft.netstrefa.pl/ultravideoxe.htm
- **Atari projects by tOri (i.e. SRAM module)**: http://atari.myftp.org/atari8bit/atari8bit.html
- **1MB SIMMExp by Pasiu/Mq** https://www.atari.org.pl/forum/viewtopic.php?id=15710
- **Sys-Check V2.2 XL/XE by Juergen van Radecke (tfhh)** https://www.van-radecke.de/STUFF/tfhh_HW_info.pdf
