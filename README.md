# ESP32_Gameboy_Printer_Link
MXW01 printer firmware for an ESP32 Game Boy Printer link.
The Game Boy link wiring and the original ESP32 printer build come from
NovenRetro: https://github.com/NovenRetro/SetupNovenRetro.
This firmware is a separate program for the MXW01 printer.



## Flash the firmware
1. Download `MXW01_ESP32_GameboyPrinterLinkV1.zip` from the Releases page and unzip it.
2. Install [Visual Studio Code](https://code.visualstudio.com/).
3. In Visual Studio Code, open Extensions and install **PlatformIO IDE**.
4. Choose **File → Open Folder** and select the unzipped `firmware` folder.
   That folder must contain `platformio.ini`.
5. Connect the ESP32 to the computer with a USB data cable.
6. On the blue PlatformIO bar at the bottom, click the right-arrow button
   **PlatformIO: Upload**.
7. The first upload also installs the ESP32 tools, so it can take several
   minutes. Wait until the terminal says `SUCCESS`.
Then click the plug icon, **PlatformIO: Serial Monitor**. The first line
should be `Picture build 19.` The monitor uses 115200 baud. Close the
monitor before uploading again, or the serial port stays busy.
If Upload cannot find the port, install the USB driver for the chip on
your board (CP210x or CH340) and try again. If the upload starts and then
fails to connect, hold the BOOT button and click Upload once more.



## Printer that was tested
This firmware was tested with a JEPEErbz model C9 mini pocket printer.
It is the small cat-shaped Bluetooth thermal printer, about 3.1 by 4.3
inches, sold as an inkless receipt and sticker printer with paper rolls
included.
Turn the printer on before you print from the Game Boy. This unit speaks
the MXW01 Bluetooth protocol. In a phone's Bluetooth list its name starts
with `MXW01`. Other cat-shaped pocket printers with that same name use the
same protocol and should work. The SC03h printer used by the original
NovenRetro firmware is a different protocol and will not print with this
file.



Schematic for soldering 6 pin GBA (quality cable) to Level Shifter to ESP32 Devkit
<img width="1280" height="754" alt="image" src="https://github.com/user-attachments/assets/5280b452-8c42-4a94-b91a-3a3a875497ed" />



ESP32 Unit used for this build
https://a.co/d/03wegyV9

Level Shifter
https://a.co/d/01wC6ynW

GBA Link Cable used
https://a.co/d/04Ra4jOz

USB C Power Unit for Battery
https://a.co/d/0bwGDkLX

On/Off Switch for USB C Power Unit
https://a.co/d/0diJCmzM

LiPo Battery pack used
https://www.aliexpress.us/item/3256812487912722.html?channel=twinner 
