Simultaneously press `Down` button and `UP` button and power on (connect to usb)

OLED will show "Call Menu"

If your system can not find drivers- download from here:
https://github.com/sparkfun/Arduino_Boards/tree/master/sparkfun/avr/signed_driver

Check serial port number on Windows Device manager "SparkFun Pro Micro (COMx)"

Using any terminal emulator, open the appropriate serial port (for example: COMx at 57600)

Press `ENTER` once.

You will see text like:
```
!!
```
If you can not see text it something wrong - DO NOT PRESS ENTER AGAIN!

Disconnect usb and check port number speed again and retry.

```
51——————
Reg 10 a27=8.50000
Reg 15 b27=18.71000
Reg 20 a144=9.00010
Reg 25 b144=15.43000
Reg 30 a433=9.03333
Reg 35 b433=14.90000
Reg 40 a868=9.00200
Reg 45 b868=15.40000
Reg 50 a915=9.00000
Reg 55 b915=15.40000
Reg 60 a1200=8.69999
Reg 65 b1200=16.63000
Reg 70 a2400=8.40000
Reg 75 b2400=15.48000
Reg 80 a5800=9.80000
Reg 85 b5800=18.91000
——————
Enter Reg
```

Backup all variable to paper first!

Trim value calculate by formula
      dBm = (sensorValue / aa);
      dBm = (dBm * -1) + bb;

So if you need to add +4db to 2400 band you need to set reg 75 b2400=15.48000  plus 4 = 19.48

To set register 75 to 19.48 you need to enter without delay 75 and wait 1 sec

You will see:
```
"reg =75
Enter call="
```

Enter without delay 19.48 and wait 1 sec

You will see:
```
"= 19.4800014495
MENU"
```
Press `ENTER` once and check 75 reg value.

Some garbage at end can be ignored.

If all ok disconnect usb and check power value.
