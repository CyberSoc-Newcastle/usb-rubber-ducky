# USB Rubber Ducky Guide
*by [CyberSoc](https://cybersoc.org.uk/?r=ducky-guide)*

*tutorials coming soon!*

If you have any issues with your ducky, feel free to ask for help at an event or contact us on our [Discord](https://cybersoc.org.uk/discord) server for assistance!

## Warning
Please use USB Rubber Duckies for educational purposes only. You follow the instructions below at your own risk. Buying one from our store or bringing your own to one of our events means you agree to the following rules:
- **Never** plug your ducky into any machine without permission from the machine owner
- **Never plug into any university machine at any time**
- **Never** leave your ducky laying around in a public place

If you break these rules, your ducky could be confiscated by either CyberSoc or the university, and you may not recieve a refund.

## Setup

It is *recommended* to use a Windows machine to program the rubber ducky, although macOS and Linux should work, we just haven't been able to test them. Any operating system that works with USB keyboards should be compatible to use as a victim machine.

There are 3 main steps to setting up your ducky, it's important to do them all and in the correct order or you will have issues programming it!

### 1) Install the Arduino IDE
Note that **you probably won’t be able to use the Arduino web editor** for this, so you will need to actually download the IDE.
- For Windows and macOS, **download** and **install** the Arduino IDE software from https://www.arduino.cc/en/software.
- For Linux, download and install the Arduino IDE from your package manager. For example in debian/ubuntu you would run `sudo apt install arduino`.

### 2) Install the Digispark extension for the Arduino IDE
1. Open the Arduino IDE you just installed, and go to **File** → **Preferences** menu at the top of the window.
2. In the **Additional Boards Manager URLs** text box, paste the following URL:
`https://raw.githubusercontent.com/ArminJo/DigistumpArduino/master/package_digistump_index.json`
3. Press **OK** to close the Preferences dialog.
4. Go to **Tools** → **Board** → **Board Manager**, again the menu is at the top of the main window.
5. Type **Digispark** into the filter box, and find the **Digistump AVR Boards** item.
6. Click **Install** on this item and wait for the board extension to install. You can close this dialog once the installation is complete.

### 3) Install the Digispark USB programming drivers
**Drivers are required for your computer to recognise programming mode** on the Digispark board. They’re only needed to upload your program - you don’t need them on victim machines for the rubber ducky to work.

#### Windows
1. Download the Windows drivers from `https://github.com/digistump/DigistumpArduino/releases/download/1.6.7/Digistump.Drivers.zip`.
2. Unzip the file somewhere and run **DPinst64.exe**.
3. Follow the instructions, and when prompted click **Install** on the Widnows Security device software dialog.

You may come accross a red security warning dialog as the drivers haven't been verified by Microsoft. If this happens, you can bypass the check by clicking **Install this driver software anyway**.

#### macOS
According to a quick Google search I did, no programming drivers are required on macOS. Your mileage may vary, if you find something that contradicts or support this then let us know!

#### Linux
**Download**, optionally inspect, **then run** the following script to install libusb and setup udev rules to allow programming of the Digispark board.
`https://raw.githubusercontent.com/sheffieldhardwarehackersandmakers/scripts/master/digispark.sh`

### 4) Done!
If you completed all the above steps successfully, you should be ready to go! We'll be posting some tutorials here soon, so keep checking back for more information on how to use and program the ducky.
