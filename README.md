👋 Hi, I’m Jeroen Taverne

I have created a multi purpose cartridge for MSX computers. It's based on a Raspberry Pi Pico clone with 16MB of FLASH memory and 256 kBytes of RAM.

For small demo videos check: https://www.facebook.com/groups/1113206428793908/permalink/6848484928599334/

The MSX Pico cartridge features:

- A 3D printed cartridge case in available colors.
- Latest version has a PCB with gold plated contacts.
- Built in menu with direct file access and very fast response.
- Built in ready to use well known ROMs.
- Built in Nextor to use micro SD card in MSXDOS2. When Nextor is used, 224 kByte extra RAM, SCC+ and Basic Kun plus is available as well
- Stereo high quality audio DAC with 3.5mm output.
- SCC+ emulation (PSG left, SCC+ right).
- Dual PSG emulation (PSG1 left, PSG2 right).
- MP3 playback in stereo (48kHz maximum sampling rate).
- RGB status LED, also used for showing audio level.
- Optional MIDI output through mini USB which uses same cable as the Midi PAC. A cable can be ordered as add-on.
- USB-C connection for firmware updates.
- ROM files with a maximum of 15MB can directly be loaded from micro SD card by the built in menu without using Sofarun or Romload.
- Automatic mapper type detection with manual adjustment. Supported mapper types: ASCII8, ASCII16, Konami with and without SCC.
- 50/60Hz video output selection
- Joystick support
- Compatible with MSX2, MSX2+, MSX Turbo R, One Chip MSX, SX1-(mini)
- Often compatible with MSX1, not guaranteed
- Often compatible with 7MHz modification, not guaranteed

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
