# MC6 Firmware Manual 

This section explains how the controller works and how pressing individual switches or different switch combinations will interact with the controller.

Please refer to the Midi Type Table as well for more information on selecting the correct midi type that you need.


## Overview
### Powering up the MC6
Your MC6 can be powered by any one of these methods:
 
* **9VDC Centre Negative** power supply
  * Connect a 9VDC centre negative power supply to the power input of the MC6.
* **9-12V AC/DC via Midi pins 6 & 7** (Phantom Power)
  * Connect a 7-pin Midi cable to the Midi Out port of the MC6. Phantom power is supplied through pins 6 and 7. Midi data from the MC6 will be sent through the other 5 pins of the same cable. The phantom power is chained to the Midi Receive pins 6 & 7, allowing you to power other devices as well.
* USB powered
  * Connect a USB cable to the MC6. It is capable of being fully powered by USB.
 
Upon power-up, the controller display will show a start screen with the model and firmware version number.

### Connections
* Midi Out/Send/Thru
  * This is where midi data is sent from the MC6 to other devices. You can use a standard 5 pin Midi cable, or a 7 pin if you require phantom power. The MC6 also receives incoming Midi data from the Midi In port and re-transmits the data to the Midi Out port. 
* Midi In/Receive
  * The MC6 is also able to receive midi messages from other devices or allow it to flow through to other devices. Phantom power from the Midi Out is chained to pins 6 & 7 on the Midi In.
* USB port
  * The MC6 can also send midi data via USB, allowing you to have control over software too.
 
### Main Configuration Menu
* Overview
  * The Main Edit Menu allows you to do the following: Factory Reset the controller, edit the Expression Input type, set the Midi Channel and set the switch sensitivity. You can access the Main Configuration page by holding down **Switch [D & F] before powering up**. The controller will boot into the Main Configuration Menu.
* Factory Reset
  * To do a factory reset, hold down **Switch [E] for 2 seconds**. The controller will indicate that it is doing a factory reset.
* MIDI Thru
  * Toggle between MIDI Thru On and Off by pressing Switch [D].
* Set Midi Receive Channel
  * Press Switch [E] to edit the MC6 MIDI receive channel. From firmware v2.2 onwards, you will be able to control the functions on the MC6 via PC and CC messages from an external Midi controller. This will allow you to quickly jump to different banks, bank up/down or call extra presets with a simple external Midi controller.
* Set Switch Sensitivity
  * From fimware v2.2 onwards, you will also be able to set the switch sensitivity. Edit this setting from the Main Configuration Menu. Select from 1 (least sensitive) to 5 (most sensitive). This is helpful when pressing dual switches to change bank, and will increase the accuracy of the bank change when it is set to a lower sensitivity.
* Edit Expression Input Type
  * You can also edit the Expression Input type from here, and choose between an Expression Pedal or Aux Switch for each expression input. In the CfgInp menu, press **Switch [A]** or **Switch [D]** to toggle between [Expn Pdl] and [Aux Sw] for each input.
  * **Please note that if you do not have any expression controllers/pedals connected, your settings should be set to [Expn Pedal]. If not, the controller will hang at the main page because the MC6 will read that a switch being pressed.**
  
### Switches and Display Labels
* Activating Presets
  * Each switch corresponds to the name on the screen that is closest to it. Pressing **Switch [A]** engages Preset A, **Switch [B]** engages Preset B and so forth.
* Editing Switches
  * To enter Edit Mode:
    1. Press the switch you wish to edit
    2. Press **Switches [D & F]** together
  * **Switch [D & F]** will bring you to the preset edit page. It will edit the last used switch/preset. Hence, if you wish to edit Switch C, press **Switch [C]** once, and then press **Switch [D & F]** to edit the settings for Switch C. If you have an external aux controller connected to the expression input, pressing a switch on the aux controller and then **Switch [D & F]** will allow you to edit the settings for that switch.
* Editing Expression Pedals
  * Similar to the Preset Edit, pressing **Switch [A & C]** will edit the settings for the last used expression pedal.
  
### Initial Preset Screen
 If you are using a new controller, or have just factory reset your controller, all the presets will be empty and the display will show [EMPTY] for each preset.
 
## Editing Presets
### Selecting A Preset To Edit
To select a preset to edit, press the switch you want to edit once. Thereafter, press down Switch [D & F] once to enter into Preset Edit Mode. The LCD will display which preset switch you are editing, before entering edit mode.

### Preset Edit Menu
* Overview
  * This page allows you to select between edit the Preset short name, full name, Midi message parameters as well as copying and pasting presets.
* Copy and pasting a preset
  * Press Switch [F] to copy a preset. When a preset is copied, the paste option will appear and is selectiable via Switch [C].
You can exit the menu and select other presets to paste the copied preset to.
* Clearing Midi Messages
  * Press and hold down Switch [E] for 1 second to reset all the Midi Messages in this preset.
* Copying a preset to all banks
  * Hold down the Switch [F] (Copy) for 2 seconds.
  * The LCD will indicate that the controller is pasting the current preset to all banks. 
* Exiting the Menu
  * Switches [D & E]: Exit menu.
  * Switches [E & F]: Exit menu.
  
### Editing Preset Messages
* Overview
  * The screen is split into different sections for different parameters. In the top row, the screen displays the Midi Message number and the Midi Message type. In the bottom row, the screen displays, from left to right, the Midi Msg number, Number 1, Value 1, Number 2, Value 2 and Channel. 
  * The parameters in the above diagram is as follows:
  
  |Parameter |Value |
  |:-------:|:---:|
  |Midi Message|1|
  |Midi Type|CC Message|
  |Number 1| 1|
  |Value 1|127|
  |Number 2|2|
  |Value 2|50|
  |Channel|1|

    * Please refer to the **Midi Type Table** on how each Message type works.
* Navigating to Next or Previous Parameter
  * The parameter that you are currently editing will be blinking. Press PREVIOUS or NEXT to go to the previous or next parameter.
* Changing Parameter Values
  * When a parameter is selected (and blinking), press VALUE UP or VALUE DOWN to adjust the paramter. Remember to save your settings by pressing Switches [D & E] before editing your next Midi Message.
* Exiting the Menu
  * Switches [D & E]: Save current Midi Message
  * Switches [E & F]: Exit menu.
  
## Editing Banks
### Bank Settings
* Overview
  * This page will allow you to edit your bank settings. To access it, press Switch [C & F] in the main preset page to enter into Bank Edit mode.
* Copy Bank
  * Press Switch F to copy the current bank that you are in.
* Paste Bank
  * After copying the bank, the PasteBank function will appear. To paste the copied bank, just change the current bank that you are in, go into Bank Edit mode and then select PasteBank. The LCD will indicate that the bank copy is complete.
* Editing Bank Name
  * Pressing Switch [D] will allow you to edit the Bank Name.
* Exit Menu
  * Press Switch [D & E] or [E & F] to exit the Bank Edit page.
  
## Editing Bank and Preset Names
### Editing Bank Name
* Overview
  * This menu allows you to edit the Bank Name for the current bank.
* Controls
  * Switch [A]: Shift the cursor back
  * Switch [B]: Shift the cursor forward.
  * Switch [C]: Shift the current selected character down
  * Switch [F]: Shift the current selected character up. 
  * Switch [D]: Jump the current character forward (e.g a -> m -> A -> M)
  * Switch [D & E]: Save and exit menu
  * Switch [E & F]: Exit the menu without saving.
  
### Editing Preset Name
Editing a preset short name and full name is similar to editing the bank name. The only difference is the number of characters available to edit for each name.

## Expression Input
### Overview
For each input, you can connect an external controller with up to 3 switches, or a 10-25k expression pedal. With this, you can have up to a total of 12 switches for your MC6 (6 external, 6 internal). Each external switch will give you the same capability and functions as an internal switch. If using an expression pedal, the MC6 is capable of sending up to 4 different Midi CC message per input, and it is bank-specific. Changing banks will allow you to send a different CC message.
 
**Important:** If you have the expression inputs set up as an Aux Switch, you need to have a stereo cable connected to the controller. If not, the controller will be stuck at the main preset page because it is reading a switch as being pressed down. To overcome this if you do not have an aux switch and stereo cable available, simply go into the Main Edit Menu and change the expression input type to [Expn Pedal].

### Setting Up The Expression Input
To edit the Expression Input Type, hold down Switch [D & F] before powering up the controller. This will boot the controller into the Main Edit Menu. Select [CfgInp] to go into the Expression Edit menu.
- Switch [A]: Toggle the expression input type between [Expn Pedal] and [Aux Switch] for Input 1.
- Switch [D]: Toggle the expression input type between [Expn Pedal] and [Aux Switch] for Input 2.
- Switch [F]: Save settings
- Switch [C]: Exit the menu

### Expression Pedal Parameters
* To enter the Expression Edit menu, press Switch [A + C] to edit the last used expression input. This is different from the Preset Edit menu, which requires you to press Switch [D + F].
* If connected via USB to the Web or Desktop Editor Application, you can access the expression pedal parameters by simply moving the expression pedal up or down and the editor will load the expression parameters.
* The MC6 will send up to 4 different Midi CC messages per input. The desired CC# goes under N1, and the range of values goes under V1 and V2. For example, using N1 = 5, V1 = 0 and V2 = 127 will send a CC#5 message with values between 0 - 127 for the full range of the expression. Setting V1 = 127 and V2 = 0 will reverse the sequence.
* Be sure you calibrate your expression pedal first. Use only expression pedals with a 10k - 25k potentiometer, with the potentiometer WIPER connected to the TIP of the TRS cable.

### Expression Display Settings
* You can select if you want the controller to show the Expression Pedal position and Expression Preset name when the expression pedal is in use. Simply go into the Expression Edit menu by pressing Switch [A & C], and click on the Display option.

### Expression Sensitivity Setting
* You can now select the sensitivity read option when using different expression pedals. The expression inputs are optimized for expression pedals with 10k linear potentiometers. Previously, using other values, like a 100k linear potentiometer, will cause the expression read to be very jittery. You can now edit the sensitivity by going into the Expression Edit menu Switch [A & C], click on the Sens option and then select the sensitivity from 1 (Lowest sensitivity) to 3 (Highest sensitivity).

## Midi Input Functions
The MC6 is able to read incoming MIDI messages. It will read messages sent to the MIDI channel that it is set to. You can send the MC6 MIDI channel from the Main Configuration menu.

|Function|CC Number|CC Value|
|:------:|:-------:|:------:|
|Bank Down|0|0 - 127|
|Bank Up|1|0 - 127|
|Preset A - L|10 - 21|0 - 127|

|Function|PC Number|
|:------:|:-------:|
|Jump to Bank| 0 - 29|

## Using The Web Editor
You can view the editor at http://editor.morningstar.io. This allows you to edit the parameters and settings on the midi controllers. All you need is an internet connection as well as the Google Chrome browser. The firmware required to use the Web Editor is v2.01 onwards.
 
1. Hold down Switch A before connect your controller to your computer via USB. The screen will indicate that it is in Editor Mode. Alternatively, toggle in and out of editor mode by pressing Switch [A & D], and then followed by Switch [F] while on the main preset page.
2. Your controller has now booted in Editor mode and will be able to communicate with the Web Editor and Google Chrome.
3. To edit a preset, scroll to your desired bank on your controller, and then press on the desired switch you wish you edit. The Bank and switch number will show on the Web Editor. 
4. Once you are done editing, click on save in the Web Editor, or just press enter. If the save is successful, it will be indicated on your controller's display.


**Important**: The Web Editor communicates with the MC6 on MIDI channel 1. Hence, if you have any devices plugged into the same computer and is receiving on MIDI channel 1, please be sure to unplug them.
  |Number 2|2|
  |Value 2|50|
  |Channel|1|

    * Please refer to the **Midi Type Table** on how each Message type works.
* Navigating to Next or Previous Parameter
  * The parameter that you are currently editing will be blinking. Press PREVIOUS or NEXT to go to the previous or next parameter.
* Changing Parameter Values
  * When a parameter is selected (and blinking), press VALUE UP or VALUE DOWN to adjust the paramter. Remember to save your settings by pressing Switches [D & E] before editing your next Midi Message.
* Exiting the Menu
  * Switches [D & E]: Save current Midi Message
  * Switches [E & F]: Exit menu.
  
## Editing Banks
### Bank Settings
* Overview
  * This page will allow you to edit your bank settings. To access it, press Switch [C & F] in the main preset page to enter into Bank Edit mode.
* Copy Bank
  * Press Switch F to copy the current bank that you are in.
* Paste Bank
  * After copying the bank, the PasteBank function will appear. To paste the copied bank, just change the current bank that you are in, go into Bank Edit mode and then select PasteBank. The LCD will indicate that the bank copy is complete.
* Editing Bank Name
  * Pressing Switch [D] will allow you to edit the Bank Name.
* Exit Menu
  * Press Switch [D & E] or [E & F] to exit the Bank Edit page.
  
## Editing Bank and Preset Names
### Editing Bank Name
* Overview
  * This menu allows you to edit the Bank Name for the current bank.
* Controls
  * Switch [A]: Shift the cursor back
  * Switch [B]: Shift the cursor forward.
  * Switch [C]: Shift the current selected character down
  * Switch [F]: Shift the current selected character up. 
  * Switch [D]: Jump the current character forward (e.g a -> m -> A -> M)
  * Switch [D & E]: Save and exit menu
  * Switch [E & F]: Exit the menu without saving.
  
### Editing Preset Name
Editing a preset short name and full name is similar to editing the bank name. The only difference is the number of characters available to edit for each name.

## Expression Input
### Overview
For each input, you can connect an external controller with up to 3 switches, or a 10-25k expression pedal. With this, you can have up to a total of 12 switches for your MC6 (6 external, 6 internal). Each external switch will give you the same capability and functions as an internal switch. If using an expression pedal, the MC6 is capable of sending up to 4 different Midi CC message per input, and it is bank-specific. Changing banks will allow you to send a different CC message.
 
**Important:** If you have the expression inputs set up as an Aux Switch, you need to have a stereo cable connected to the controller. If not, the controller will be stuck at the main preset page because it is reading a switch as being pressed down. To overcome this if you do not have an aux switch and stereo cable available, simply go into the Main Edit Menu and change the expression input type to [Expn Pedal].

### Setting Up The Expression Input
To edit the Expression Input Type, hold down Switch [D & F] before powering up the controller. This will boot the controller into the Main Edit Menu. Select [CfgInp] to go into the Expression Edit menu.
- Switch [A]: Toggle the expression input type between [Expn Pedal] and [Aux Switch] for Input 1.
- Switch [D]: Toggle the expression input type between [Expn Pedal] and [Aux Switch] for Input 2.
- Switch [F]: Save settings
- Switch [C]: Exit the menu

### Expression Pedal Parameters
* To enter the Expression Edit menu, press Switch [A + C] to edit the last used expression input. This is different from the Preset Edit menu, which requires you to press Switch [D + F].
* If connected via USB to the Web or Desktop Editor Application, you can access the expression pedal parameters by simply moving the expression pedal up or down and the editor will load the expression parameters.
* The MC6 will send up to 4 different Midi CC messages per input. The desired CC# goes under N1, and the range of values goes under V1 and V2. For example, using N1 = 5, V1 = 0 and V2 = 127 will send a CC#5 message with values between 0 - 127 for the full range of the expression. Setting V1 = 127 and V2 = 0 will reverse the sequence.
* Be sure you calibrate your expression pedal first. Use only expression pedals with a 10k - 25k potentiometer, with the potentiometer WIPER connected to the TIP of the TRS cable.

### Expression Display Settings
* You can select if you want the controller to show the Expression Pedal position and Expression Preset name when the expression pedal is in use. Simply go into the Expression Edit menu by pressing Switch [A & C], and click on the Display option.

### Expression Sensitivity Setting
* You can now select the sensitivity read option when using different expression pedals. The expression inputs are optimized for expression pedals with 10k linear potentiometers. Previously, using other values, like a 100k linear potentiometer, will cause the expression read to be very jittery. You can now edit the sensitivity by going into the Expression Edit menu Switch [A & C], click on the Sens option and then select the sensitivity from 1 (Lowest sensitivity) to 3 (Highest sensitivity).

## Midi Input Functions
The MC6 is able to read incoming MIDI messages. It will read messages sent to the MIDI channel that it is set to. You can send the MC6 MIDI channel from the Main Configuration menu.

|Function|CC Number|CC Value|
|:------:|:-------:|:------:|
|Bank Down|0|0 - 127|
|Bank Up|1|0 - 127|
|Preset A - L|10 - 21|0 - 127|

|Function|PC Number|
|:------:|:-------:|
|Jump to Bank| 0 - 29|

## Using The Web Editor
You can view the editor at http://editor.morningstar.io. This allows you to edit the parameters and settings on the midi controllers. All you need is an internet connection as well as the Google Chrome browser. The firmware required to use the Web Editor is v2.01 onwards.
 
1. Hold down Switch A before connect your controller to your computer via USB. The screen will indicate that it is in Editor Mode. Alternatively, toggle in and out of editor mode by pressing Switch [A & D], and then followed by Switch [F] while on the main preset page.
2. Your controller has now booted in Editor mode and will be able to communicate with the Web Editor and Google Chrome.
3. To edit a preset, scroll to your desired bank on your controller, and then press on the desired switch you wish you edit. The Bank and switch number will show on the Web Editor. 
4. Once you are done editing, click on save in the Web Editor, or just press enter. If the save is successful, it will be indicated on your controller's display.


**Important**: The Web Editor communicates with the MC6 on MIDI channel 1. Hence, if you have any devices plugged into the same computer and is receiving on MIDI channel 1, please be sure to unplug them.
