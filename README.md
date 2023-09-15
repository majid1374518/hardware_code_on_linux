# hardware_code_on_linux
This is my hardware workaround on Linux and its documentation
***
# For writing code on AVR chipsets get help from the below commands:
## Install the below packages:
```sudo apt-get install gcc-avr binutils-avr avr-libc gdb-avr avrdude```

To make a script to compile the code write the content of the blow text save it into the file and make it executable:

```
#!/bin/bash
avr-gcc -Wall -g -os -mmcu=$1 -o $2.bin $2.c
avrdude -p $1 -c $3 -U flash:w:$.hex -P usb
```

Then make it executable with ```chmod 755 /path/to/this/file```.
run the file and code will upload to your device.
***
