GUIDA:
https://geekhack.org/index.php?topic=14290.0

https://github.com/tmk/tmk_keyboard/tree/master/converter/adb_usb

cd /home/dbarchetta/Documenti/tmk_keyboard/converter/adb_usb

make -f Makefile clean
make -f Makefile.rev1

reset tra pin rst e gnd, forse 2 volte

avrdude -u -p atmega32u4 -P /dev/ttyACM0 -c avr109 -U flash:w:adb_usb_rev1.hex
