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

- February rollover bug in the original release (rolled over Feb 09 → Feb 29)
- Leap-year logic updated to follow the Gregorian calendar, ensuring February 29 appears only in valid leap years
- Note: The GBA RTC supports only 2000–2099; the Gregorian leap-year logic is implemented for correctness and potential future use beyond 2099
