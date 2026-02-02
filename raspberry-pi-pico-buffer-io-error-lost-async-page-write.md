## Raspberry Pi Pico - Buffer I/O error with lost async page write - unable to read boot sector error

If you encounter this (flashing different firmwares is what I have seen as the trigger) then a solution is erasing all of the flash with a special file provided as part of [the documentation](https://www.raspberrypi.com/documentation/microcontrollers/pico-series.html#resetting-flash-memory) which links to [this UF2 file](https://datasheets.raspberrypi.com/soft/flash_nuke.uf2) and the [code on GitHub](https://github.com/raspberrypi/pico-examples/blob/master/flash/nuke/nuke.c). Also [found here among the repositories of the Pico Keys maker](https://github.com/polhenarejos/pico-nuke).

### Path to this solution when not a lot of search results for the Pi Pico buffer I/O error

I didn't see a lot of results for this error online [this Raspberry Pi forum post being one of the few](https://forums.raspberrypi.com/viewtopic.php?t=369153) and I found the answer to the error via searching for "pi pico factory reset" and [this Raspberry Pi forums post discussing the flash_nuke.uf2 as a universal firmware file suitable for Pico and Pico 2](https://forums.raspberrypi.com/viewtopic.php?t=383975).
