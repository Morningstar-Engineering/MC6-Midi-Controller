# MC6 Firmware Manual 
This section explains how the controller works and how pressing individual switches or different switch combinations will interact with the controller.

Please refer to the Midi Type Table as well for more information on selecting the correct midi type that you need.

## POWERING UP THE MC6
Your MC6 can be powered by any one of these methods:
* 9VDC Centre Negative power supply
  * Connect a 9VDC centre negative power supply to the power input of the MC6.
* Phantom Power (9-12v AC/DC)
  * Connect a 7-pin Midi cable to the MIDI OUT port of the MC6. Phantom power is supplied through pins 6 and 7. Phantom power is chained to pins 6 & 7 on the MIDI IN port as well, allowing you to power other devices.
* USB powered
  * Connect a USB cable to the MC6. The MC6 is capable of being fully powered by USB.
 
## Connections
* Midi In/Receive
  * This is where the MC6 receives MIDI messages from other MIDI devices.
* Midi Out/Send/Thru
  * This is where MIDI data is sent from the MC6 to other devices. You can use a standard 5-pin MIDI cable, or a 7-pin one if you want to power the MC6 with phantom power. The MC6 also has MIDI THRU, which allows incoming MIDI messages to be relayed to other MIDI-capable devices.
* USB port
  * The MC6 can also send and receive MIDI data via USB, allowing you to have control over your DAWs and music software. It is class compliant and compatible with Windows, OSX and iOS.
* EXP 1 & 2
  * Connect your expression pedals to these ports. You may also connect aux switches here to add more programmable switches to the MC6.

## GLOBAL CONTROLLER SETTINGS
### Accessing Controller Settings:
To access the Controller Settings Menu, hold down switches [D + F] while powering up the MC6.


### mThru
Switch on/off the MIDI thru function on the MC6. This function allows the MC to relay MIDI messages from other devices to devices further down the MIDI chain.

### Reset
To do a factory reset, hold down for 2 seconds. The MC6 will show that it is performing a factory reset. All user presets and settings will be lost when a factory rest is done. 


### MidiCh
Set the MIDI receive channel for the MC6. The MC6 can receive messages from external midi controllers.

### ChgInp
Change Expression Input Type. The two 1/4 inch inputs on the MC6 can each be used independently for expression pedals or external aux switches.

**IMPORTANT** - Please note that if you do not have any expression pedals/external switches connected to the MC6, your Expression Inputs should be set to [Expn Pedal]. Otherwise the MC6 will hang on the main page as it will think that an external switch is being pressed.

### SwSens
Set switch sensitivity. Choose from 1 (least sensitive) to 5 (most sensitive). By default, this is set to 3 and should be comfortable for most users. Depending on personal taste, you may adjust sensitivity to help you bank up/down (by stepping on 2 switches at once) more accurately.

## SCROLLING THROUGH BANKS
###Scrolling through Banks
Step on switches [A + B] together to bank down and switches [B + C] to bank up. There are a total of 30 banks of 6 programmable switches on the MC6.

## SWITCHES AND DISPLAY NAMES
### Activating Presets
Each switch corresponds to the display name closest to it. Pressing switch [A] activates Preset A, switch [B] activates Preset B and so forth.

## PROGRAMMING SWITCHES
On a new controller, all switches are initially labelled as EMPTY. It is up to you to decide exactly what each one will do.

To program a switch:
1. Press the switch you wish to program
2. Press Switches [D + F] together. This will take you the the Switch Settings Menu shown below.

### Msg
Edit the MIDI message that will be sent by each switch.

Use switches [A] and [B] to move between parameters, and switches [F] and [C] to increase and decrease parameter values. At any time, press [D+E] together to save your current message settings, and press [E+F] to return to the previous menu without saving.

* M: This is the message number of the MIDI message that you are editing. Each switch on the MC6 can send up to 8 different MIDI messages at once. Press to scroll through the 8 messages to edit each one. 
* Type: Choose the type of MIDI message you want to send. You can select from Program Change (PC), Control Change (CC), Toggle messages and many others. Please refer to our MIDI Message Types List on page 15 for the full list of messages available and what each one can do.
* 0:0: The first pair of zeros you see on the screen are Number 1 : Value 1. Each parameter on your other MIDI devices have corresponding MIDI numbers. By changing MIDI Number 1, you can choose which parameter you want to affect on your other devices. By changing you MIDI Value 1, you set the value you want the chosen parameter to be at. 
* 0:0: The second pair of zeros you see on the screen are Number 2 : Value 2. These are required only when you use toggle type MIDI messages, allowing you to toggle between Number 1 : Value 1 and Number 2 : Value 2 using the same switch.
* Ch: This determines the MIDI channel (1-16) that your MIDI message will be sent through. Assign different MIDI channels of each of your other devices so that messages for specific devices will not conflict with each other. 

### Clear
Hold down to clear all settings on current switch.
### Copy
* Press to copy the settings of the current switch.
* **IMPORTANT** - Holding down this switch will copy and paste this particular switch’s settings to the same switch across all banks. Do not hold down this switch if you do not wish for this to happen. 

### Paste
* Press to paste copied switch settings onto current switch.

### Name
* Name your switches. This will be displayed on the main screen of the MC6.

* Use switches [A] and [B] to move between characters, and switches [F] and [C] to change characters. Pressing switch [D] allows you to skip characters and scroll through more quickly. At any time, press [D+E] together to save your current settings and exit, or press [E+F] to exit without saving.

**HANDY TIP: Quick Scroll through Common Names**
Some common names have been pre-programmed for your convenience. Use switches [A+B] and [B+C] to scroll through them.


### FullName
Choose a longer name for the selected switch. This name will be displayed when the switch is stepped on. If left blank, no full name will be shown when the switch is stepped on.

## BANK SETTINGS

### ACCESSING BANK EDIT MODE
On the home screen, press switches [C+F] to enter Bank Edit mode shown below.


### BankName
Name your current bank. Naming banks is done the same way as naming switches. Please refer to page 9.
### Copy
Copy current bank settings. All bank and switch settings on the current bank will be copied to clipboard.
### Paste
Paste copied bank settings to current bank.

## USING EXPRESSION PEDALS
### Programming Expression Pedals
Similar to programming switches, pressing Switch [A + C] will allow you to program your last moved expression pedal.

### Expression Pedal Settings Menu

### Edit
Choose what you want your expression pedal to control. Be sure to calibrate your expression pedal first (see below). Use only expression pedals with 10k to 25k potentiometers, with wiper to tip.

Programming expression pedals is very similar to programming switches (refer to page 8). The CC number for your expression pedal message is represented by Number 1 and the range of values sent will be from Value 1 to Value 2. Each expression pedal can send up to 4 MIDI messages.

### Sens
Adjust the sensitivity level of your expression pedal.

### Calibrate
Calibrate your expression pedal by setting the Heel Down and Toe Down positions.

### Display
When this feature is enabled, your expression pedal’s name (as named by you) and the expression pedal’s position will be displayed when the pedal is being moved.

## USING EXTERNAL CONTROLLERS
You can connect external Aux or Midi controllers to your MC6 and expand its functionality and capability.

### Aux Switch Controllers
Connect your aux switches (eg. Morningstar SE3 Switch Expander available on our website) via stereo 1/4” cables to the expression inputs of the MC6. Each expression input can accept up to 3 aux switches. This will give you 6 more fully programmable switches (that’s a total of 12 switches).

### Midi Controllers
Connect an external Midi controller to the MIDI IN of the MC6. This will allow you to control specific functions on the MC6, such as jumping immediately to specific banks, adding extra switches or banking up and down with your external Midi controller. 

The MC6 is able to read incoming MIDI messages. It will read messages sent to the MIDI channel that it is set to. You can set the MC6 MIDI channel from the Global Controller Settings menu (refer to page 3). The functions you can control include:

|Function|CC Number|CC Value|
|:------:|:-------:|:------:|
|Bank Down|0|0 - 127|
|Bank Up|1|0 - 127|
|Preset A - L|10 - 21|0 - 127|

|Function|PC Number|
|:------:|:-------:|
|Jump to Bank| 0 - 29|

## MC6 EDITOR (MAC AND PC COMPATIBLE)
A software editor is available for you to program your MC6 switches even more quickly and easily. 

Download the MC6 Editor from our downloads page at:
http://www.morningstarfx.com/downloads

### Using the MC6 Software Editor
1.	Connect your MC6 to your computer via the included USB cable. 
2.	On the home screen of your MC6, hold down switches [A+D] and then press [F] to enter Editor mode. Only then can the Software Editor detect the MC6 controller.
3.	To program a switch, just press on the switch you wish to program. It’s bank number and switch letter will be displayed on the Software Editor’s screen.
4.	Name your switch, and input the parameters and values you wish to use.
5.	Click on ‘Save’ or hit Enter to save your switch’s name and message settings.

### Using The Web Editor
You can view the editor [here](https://web-editor-88874.web.app/). This allows you to edit the parameters and settings on the midi controllers. All you need is an internet connection as well as the Google Chrome browser. The firmware required to use the Web Editor is v2.01 onwards.

**IMPORTANT** - The MC6 Software Editor communicates with the MC6 on MIDI channel 1. If, you have any devices plugged into the same computer and receiving messages on MIDI channel 1, please be sure to unplug them to avoid conflicting messages.

## UPDATING FIRMWARE
We work on firmware updates to continually improve your MC6 experience.

Download the MC6 Updater Software and latest Firmware Updates from our downloads page at:
http://www.morningstarfx.com/downloads

Connect the MC6 to your computer via the included USB cable, and use the Updater Software to upload the latest firmware to your controller.
