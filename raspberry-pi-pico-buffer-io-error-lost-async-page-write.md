## Raspberry Pi Pico - Buffer I/O error with lost async page write - unable to read boot sector error

```
[ 3647.497271] device offline error, dev sdb, sector 260 op 0x1:(WRITE) flags 0x0 phys_seg 1 prio class 2
[ 3647.497290] Buffer I/O error on dev sdb1, logical block 259, lost async page write
[ 3647.545527] FAT-fs (sdb1): unable to read boot sector to mark fs as dirty
```

If you encounter this error - as seen in above [dmesg](https://en.wikipedia.org/wiki/Dmesg) output - while using a Pico (flashing different firmwares is what I have seen as the trigger) then a solution is erasing all of the flash with a special file mentioned/provided as part of [the documentation](https://www.raspberrypi.com/documentation/microcontrollers/pico-series.html#resetting-flash-memory) which links to [this UF2 file](https://datasheets.raspberrypi.com/soft/flash_nuke.uf2) and the [code on GitHub](https://github.com/raspberrypi/pico-examples/blob/master/flash/nuke/nuke.c). Also [found here among the repositories of the Pico Keys maker](https://github.com/polhenarejos/pico-nuke).

### Path to this solution when not a lot of search results for the Pi Pico buffer I/O error

I didn't see a lot of results for this error online [this Raspberry Pi forum post being one of the few](https://forums.raspberrypi.com/viewtopic.php?t=369153) (apart from mine having flags value 0x0 and using sdb1 it is an identical error message - same sector 260 and logical block 259 and inability to read boot sector) and I found the solution to the error (in form of the flash_nuke.uf2) via searching for "pi pico factory reset" and [this Raspberry Pi forums post discussing the flash_nuke.uf2 as a universal firmware file suitable for Pico and Pico 2](https://forums.raspberrypi.com/viewtopic.php?t=383975).
