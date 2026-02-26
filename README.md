# GBA RTCRead (Fixed)

This tool can read and write the RTC found inside certain GBA cartridges (Pokémon Ruby/Sapphire/Emerald and Boktai games).

The original tool and details about the RTC chip were documented here: [http://www.furlocks-forest.net/wiki/?page=Pokemon_Ruby/Sapphire_New_Battery_Glitch](https://web.archive.org/web/20180413154901/http://www.furlocks-forest.net/wiki/?page=Pokemon_Ruby/Sapphire_New_Battery_Glitch)

The DS port is still available here: [https://sourceforge.net/projects/rtcread-ds/](https://sourceforge.net/projects/rtcread-ds/)


## Features

- Read current date and time from the RTC 
- Write new date and time to the RTC 
- GBA version must be run from a GBA flashcart and works via cartridge swap
- GBA version can also edit the RTC on Everdrive GBA cartridges
- DS version is a homebrew for R4 carts that access GBA cartridges via Slot-2 insertion

## Known Issues

- None at the moment

## Fixed Issues

- Both the original GBA and DS releases contained a February leap-year rollover bug, where the date incorrectly rolled over on Feb 09 instead of Feb 29
- The original implementation assumed every fourth year is a leap year (year % 4 == 0), which incorrectly treats certain century years (e.g., 2100) as leap years
- Note: The GBA RTC only supports years 2000–2099 (program accepts 00–99). Century leap-year rules (e.g., 2100 not being a leap year) do not affect gameplay; this logic is included for correctness and future-proofing
