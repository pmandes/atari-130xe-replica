# Atari 130XE (64x4) Assy No. CA200519 motherboard replica

This is a replica of the motherboard of a Atari 130XE 8-bit computer. It was created on the basis of the last version of the board - "CI03579 REV.1 / Assy No. CA200519" - which was mounted in last batches of Atari 65XE, Atari 800XE and Atari 130XE.

It differs from previous versions primarily by using 2/4 memory chips instead of 8 in the Atari 65XE or 16 in the Atari 130XE. It also features a full ECI/CART connector, which was missing in earlier versions of the 65 series. This replica is reproduced almost exactly 1:1 from the original, with only the descriptive layer modified for greater clarity. There may also be other minor improvements, such as the removal of certain errors present in the original.

## The purpose of the project: ##
I created this project mainly out of nostalgia for the 8-bit Atari I had in my childhood, inspired by projects like the [ReAmiga 1200](https://www.reamiga.info/?page_id=38) by Chucky or [C64 Replica](https://github.com/bwack/C64-250407-Replica-KiCad) by bwack. My intention was not to build a board enhanced with modern modules and extensions, such as the [1088 XEL](https://ataribits.weebly.com/1088xel.html). I wanted my replica to be as close to the original as possible, with only minor improvements. But above all, it is a substitute onto which you can transplant the original components from your damaged motherboard, which may be rusty, have burnt traces caused by unprofessional repairs, upgrades or memory replacements. Your Atari will gain new life with a high-quality motherboard and a great appearance.

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

### Other ICs: ###
| No | Chip | Original part | Description |
|--------:|----------------------------|:--------------------:|:------------------|
|U9,U10,U11,U12|4464|Sharp LH2464-12|DRAM memory (4464 compatible)|
|U24,U25|4051|Toshiba TC4051BP|Single 8-channel multiplexer/demultiplexer|
|U1|LM358|Texas Instruments LM368N| Low-voltage audio power amplifier|
|U2|74LS138| |3-line to 8-line decoder / demultiplexer|
|U3|MMU|Atari C061618|Memory Management Unit|
|U34|EMMU|Atari C025953| Extended Memory MU for 128kB *|
|U20|4050|CD4050| CMOS Hex Buffer |


* It occurs in Atari 130XE computers. It can be replaced by a [GAL chip](https://github.com/mikulski-lab/C25953-emmu). In the 65XE version, there are 0 Ohm resistors.
  You can simply connect the corresponding pins with short wires, as shown in the picture: 

<p align="center"><img src="https://raw.githubusercontent.com/pmandes/atari-130xe-replica/main/images/64k-mode.png" width="300"></p>

### Crystals: ###

| No | Chip | PAL | NTSC |
|--------:|--------------|:--------:|:--------|
|Y1|HC18/HC49 case|14.187576 MHz	|14.31818 MHz|
|Y2|HC18/HC49 case|4.433618 MHz  | - |


## Motherboard: ##

<p align="center"><img src="https://raw.githubusercontent.com/pmandes/atari-130xe-replica/main/images/130xe-replica-1.0.jpg" width="480"></a>
<img src="https://raw.githubusercontent.com/pmandes/atari-130xe-replica/main/images/atari-130XE-replica-syscheck.png" width="480"></a></p>

## Changleog: ##

**1.1 (March 2025)**
- corrected minor mistakes in the prototype, iBOM updated

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

## Other replicas: ##
- **ZX Spectrum 48k ISSUE 6A**: https://github.com/pmandes/zx-spectrum-issue6a-replica
- **Atari 800XL** by ezcontents: https://ezcontents.org/atari-800xl-pcb-remake
- **Atari 600XL** by kveldulfur: https://www.kveldulfur.de/600xl-pcb/
- **Commodore C64 Assy 250407** by bwack: https://github.com/bwack/C64-250407-Replica-KiCad
- **Commodore C64C Assy 250469** by bwack: https://github.com/bwack/C64C-250469-KiCAD-Replica
- **ReAmiga 1200/3000** by Chucky: https://www.reamiga.info/
 
---
All material published here is under a [Creative Commons 4.0 license](https://creativecommons.org/licenses/by-nc-nd/4.0/).

<img src="https://raw.githubusercontent.com/pmandes/atari-130xe-replica/main/images/Cc_by-nc-nd_icon.png" width="150">

**Atari and the Atari logo are registered trademarks of Atari Interactive, Inc.**
