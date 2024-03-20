👋 Hi, I’m Jeroen Taverne

I have created a multi purpose cartridge for MSX computers. It's based on a Raspberry Pi Pico clone with 16MB of FLASH memory and 256 kBytes of RAM.

For small demo videos check: https://www.facebook.com/groups/1113206428793908/permalink/6848484928599334/

The MSX Pico cartridge features:

- 3D printed cartridge case in available colors
- PCB with gold plated contacts.
- Built in menu
- Stereo 3.5mm audio output
- FMPAC sound en SRAM emulation
- Konami SCC+ sound emulation
- Dual PSG sound emulation
- MP3 player
- Volume en mono/stereo setting
- Micro SD card slot
- USB-C connector for software update
- RGB status LED
- Optional MIDI uitgang
- Nextor and turbo BASIC built in
- At most 224kB extra RAM avilable for Nextor
- ROM files till 15MB supported
- DSK files till 720kB supported (multi disk support is in development)
- ASCII, Konami, NEO mapper support
- For MSX2, MSX2+, TurboR computers
- Works on most MSX1 computers
- Sony XV-T550 support

For a questions, ideas and orders please contact: msxpico@gmail.com

MANUAL

Never insert or remove the cartridge when the MSX is powered on!
 
Built in menu:
After inserting the cartridge and power up a selection menu is shown on screen. It’s a selection of Nextor, fixed Konami games, ASCII games and a SCC demo. All these items can be started without a SD card inserted. Games with SCC will also produce SCC sound. For the Nextor manual, check the Nextor website.

By pressing the right cursor key the SD card contents is shown. In this screen the following files can be started:

-	.ROM files (support for standard ROMs, ASCII 8, ASCII 16, Konami without SCC and Konami with SCC sound)
-	.MP3 and .WAV files (48 kHz max)

Help screen:
Help page is shown by pressing the H key
Configuration screen is shown with SHIFT+H key

Disk images:
Please use Nextor with Sofarun. Make sure the SD card if formatted at FAT16. This can be forced by using Nextor format utility. Type call fdisk in BASIC to create partitions and format the SD card.

SCC+ implementation:
The SCC+ emulation currently involves the sound chip only. Konami ROMs will work without any modifications. VGMPLAY and SOFARUN can detect the SCC+ without any issues. To be able to detect the SCC+ properly by for instance SD Snatcher, the modified version of game need to be used. This might also apply to other games or demos.

RGB LED:
-	Purple when connected to PC by USB-C for software update
-	Green steady when software update is finished
-	Green blink when SD card is accessed when Nextor is used
-	Red blink when MSX is reset
-	Blue blink when MIDI data is sent
-	White fading when audio is played

Create bootable SD card:
- Insert MSX Pico
- Power on the MSX
- Select Nextor
- Insert new SD card
- In BASIC type: call fdisk
- Select the SD card
- Delete all partitions by pressing D key
- Create at least one new partition by pressing A key
- Write the parititions by pressing W key
- Power off the MSX
- Copy the contents of msxpico_sd.zip to the first partition using a PC or MAC
