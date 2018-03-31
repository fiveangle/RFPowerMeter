  Press Down button and UP Button AND power on (connect to usb)
OLED will show "Call Menu"

if you system can not find drivers- download from here
https://github.com/sparkfun/Arduino_Boards/tree/master/sparkfun/avr/signed_driver


download any terminal software
i use http://www.ayera.com/teraterm/ttpro313.zip

check serial port number on Windows Device manager "SparkFun Pro Micro (COMx)"

Open terminal window COMx at 57600,

press once ENTER.

you see text like

!!
if you can not see text it something wrong - do NOT PRESS ENTER AGAIN!
disconnect usb and check port number speed and over option.


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


backup all variable to paper first!


trim value calculate by formula
      dBm = (sensorValue / aa);
      dBm = (dBm * -1) + bb;

so if you need add +4db to 2400 band you need 
set reg 75 b2400=15.48000  plus 4 = 19.48

to set register 75 to 19.48 you need

enter without delay 75 and wait 1 sec
you see
"reg =75
Enter call="

enter without delay  19.48 and wait 1 sec
you see 
"= 19.4800014495
MENU"
press once ENTER.

and check 75 reg value.

some garbage at end it is normal- it is Arduino ;-)


if all ok disconnect usb and check power value