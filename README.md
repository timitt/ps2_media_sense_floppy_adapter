# PS/2 Media Sense Floppy Adapter

This adapter allow to use standard floppy drive or Gotek drive (with FlashFloppy firmware) on IBM PS/2 computers
that have Media Sense drives.

Adapter allows to be configured to 1.44 MB and 2.88 MB FDD drive with Media Sense.

It should be possible to use multiple drives with this adapter.

1.2 MB FDD mode is currently untested. My guess is that 1.2 MB drive can't be used as A drive.

## Jumpers

If neither 1.2 floppy and 2.88 floppy jumpers are shorted then drive is 1.44 MB floppy.

Shorting JP1 pins 2 and 3 (bottom ones) you send density info from computer which is normal way floppy drives work.
However later 1.44 MB and likely 2.88 MB drives do not use this signal.

Gotek can be configured to send density info from drive and therefore actually send Media Sense info.
This only works when drive is 1.44 MB drive. In this case you short JP1 pins 1 and 2 (top ones) and JP2.

Typically JP1 and JP2 can be without jumpers and all works well.

## Resistor Network

Resistor network is not needed with Gotek drive as it has 1kOhm pull up resistors already.

Only 6 pin resistor network is needed. Rest are unused.

Possible options for resistance are 1kOhm, 4.7kOhm or 10kOhm. Tests are done with 4.7kOhm resistor network.

## Building

Everything is through hole stuff and easy to solder.

GAL16V8D chip can be programmed with TL866 programmer using JED file in gal folder.

It is highly recommended to use quite short cable between adapter and floppy drive.
Long cables seem to cause random errors.

## Tested Computers

* PS/2 Model 40 SX

(Feel free to report other working machines)

## License

(c) Timi Tuohenmaa, 2023

This work is licensed under CC BY 4.0. To view a copy of this license, visit http://creativecommons.org/licenses/by/4.0/
