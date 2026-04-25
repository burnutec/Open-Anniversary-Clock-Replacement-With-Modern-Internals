# Open-Anniversary-Clock-Replacement-With-Modern-Internals

DISCLAIMER:
The modifications you do to your equipment , i can not be held responsible.
The software and models are provied free of charge , what you do with them i can not be held responsible for.
This is a hobby project i decided to share , comes without any warranties.

So after reading this lets begin:

Originally Called The Floating Display Clock
Because in the dark all you can see is the 2 displays , yes it has 2 , that gives more possibilities in terms of use and displaying information.
The parts make out the housing are printed with transparent PLA for the same reason , to be invisble :).

Keep in mind , i'm not a 3d design expert , nor a programmer , or electrical engineer.
More a hobbist maker - developer - technician.

This project is aimed at creating all the internals for a  replacement clock , made to fit inside a middle sized clock dome , wheter it is acrylic or glass , its up to you in the finishing touches. 
The electronics are designed to be as cheap and available as possible , with the exception of the melody chip, that is obtainable , but availablility is somewhat in debate.
The chip HK221-2 is from a company Honistak in taiwan , and currenty in production , obtaining it will still be challenging if not bought in quantity.
The chip seems to be a clone / reproduction of the UM3482A which is also from a Taiwanese company UMC from the early 90's. I have chosen this chip because it has retrigger input and very few support components.
The chips used for development are obtined from this website: https://www.budgetronics.eu/en/ics/special-use-ics/multi-tunes-melody-ic-hk221-2/a-6563-10000142
The brains of the operation is the ESP32-C3 Supermini , which is widely available , and cheap but capable.
Sensors are AHT20+BMP280 module , also readily available internet wide.
For Light sensing , GL5528 is used in a resitor divider configuration.
RTC the legendary DS3231 , yes no crystals needed and accurate enough for longer timekeeping compared to the DS1307 most pepole use. RTC battery is CR1220 for compactness.
A simple one tramsistor amplifier is used for playing the molodies from the HK221-2 , with an 8R 0.5W speaker is an ideal choice in 50mm diameter.
RT9013-33GB used for voltage regulation , small cheap and widely available.
Two TM1637 LED display driver for the screens.
The clock has no keys or buttons , all inputs handled with IR remote control. VS1838 compatible receiver used to decode the remote control commands.

Current fucntions:

- Display Time 
- Display Date
- Display in 12 / 24HR format
- Display Temperature 
- Display Humidity 
- Display Air pressure
- Display Currently set Time mode 12/24HR
- Display Week number
- Manual brightness setting 1-7
- Automatic Brightness setting ( Based on environmental light ) - Can be set to ON/OFF
- Hourly Chime  - Can be set to ON / OFF
- WIFI clock sync using NTP , requires setup , toggled from Remote control.
- Check for Alarm 1 or 2 is ON or OFF

In development : Alarm function

                                                                                                       



