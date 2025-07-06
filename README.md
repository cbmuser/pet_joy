# pet_joy
CBM Pet Joystick, Wifi and CB2-Sound

The adapter is connected to the Userport and uses the 8 bit I/Os and the handshake-line for the additional hardware. There are three joystick-ports, a dual-joystick and the "Stupid PET Tricks"-port. The ports, also CB2 used for 1bit-Sound are switchable to the Wifi-modem by a 74LS257 Multiplexer and a jumper. 
It uses the known, modded C64 Wifi-Modem software and a Wemos D1 Mini. Unfortunally in this first version are 300 up to 1200 Baud possible. 2400 Baud causes transfer-errors and I still must discover the issue. It was only tested with the second PET board 2001N.
For the CB2-line a seperate jumper is included to disconnect the LM386 amplifier, because in Wifi-mode it will produce aggy Rx-responses on the audio-line.

## Joystick-Ports

<code>
Dual-Joystick
[PA0] UP     ---> Fire
[PA1] DOWN   ---> Fire
[PA2] LEFT
[PA3] RIGHT
[PA4] UP    ---> Fire 
[PA5] DOWN  ---> Fire
[PA6] LEFT
[PA7] RIGHT
Fire (Sub-D Pin 6) is coupled by two ports and two 4148 diodes. 

Stupid PET Tricks (Single Joytsick)
[PA0] LEFT
[PA1] RIGHT
[PA2] UP
[PA3] DOWN
[PA4] UNUSED
[PA5] FIRE
[PA6] UNUSED
[PA7] UNUSED
</code>

## CB2-Sound
For driving and decoupling the CB2-Sound a LM386 driver is included. You can adjust the volume by the 10K potentiometer. It is only a small gain-stage (max. x20) to drive a 1 Watt/8Ohm speaker.

## WIFI-Modem
With the Wifi-Modem you'll able to connect your PET to a BBS by Telnet and the PETTERM. It uses the known, modded firmware for the WEMOS D1 NodeMCU. 



## PCB
![PCB](https://github.com/cbmuser/pet_joy/blob/main/images/pcb.png)
With the JOY/WIFI-Jumper you can swich between Joystick (open) oder Wifi (closed). With the Jumper near the LM386 you can cut the audio-line. On the right, below Joystick#1-port you can connect a small speaker. 

>[!CAUTION]
>The supply must be 5V+ ! You can uses the JST-connector or the USB-3 charge-port.

## Links

http://www.mediafire.com/file/tm71a1oa1a3macc/alwyz_modded_firmware.rar
https://github.com/ChartreuseK/PETTERM

### Games
Old: https://archive.org/details/softwarelibrary_pet or https://portcommodore.com/files/petfiles.htm

New: https://itch.io/games/tag-commodore-pet












