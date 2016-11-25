# MC6 Midi Types Reference
  Each preset contains 8 messages and sends them out in chronological order from message 1 to message 8.
  Each Midi Type consists of 6 different parameters: <b>Type, Number, Value 1, Value 2 and Channel</b>.
  
  Depending on the Midi Type you choose for each message, the numbers and values will be used differently.

# Message Descriptions
## Empty Message
| Midi Type        | Number1         | Value1        |Number2        | Value2         | Details|
|:----------------:|:----------------:|:--------------:|:--------------:| :--------------:| :--------------:|
| Empty Message    | - | - | - | - | - |

**Description**
No data will be sent out.


## Program Change
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |0 - 127           |-              | -             | -              |1 - 16           |
| **Details**   |PC Number           |-|-|-|-|

**Description**
Sends a Program Change message of a specified number and channel. Program Change messages are usually used to call presets or patches in your Midi devices.
 
**Example of Use**
Activate a preset/patch on your Midi Device.

## Control Change
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |0 - 127           |-              | -             | -              |1 - 16           |
| **Details**   |CC Number|CC Value| -| -| - |


**Description**
Sends a Control Change message of a specified number, value and channel. Control Change messages are usually used to change function parameters or call functions in your Midi devices.

If you need a CC message sent continuously when the switch is held down, set N2 = 127 and V2 = 127.
 
**Example of Use**
To activate the record function on the Strymon Timeline, send a CC message of Number 1 = 87 and Value 1 = Any 
(Refer to Timeline Manual)

## PC Toggle
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |0 - 127           |-              | 0 - 127             | -              |1 - 16           |
| **Details**   |PC Number (Inactive) | - | PC Number (Active) | - | - |
**Description**
This Midi message toggles between two Program Change message each time the switch is pressed down. Step once to send a PC message with Number 1, and step again to send a PC message with Number 2.
 
**Example of Use**
You can easily toggle between two presets with this message.

## CC Toggle
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |0 - 127           |0 - 127              | 0 - 127             | 0 - 127              |1 - 16           |
| **Details**   |CC Number (Inactive) |CC Value (Inactive) |CC Number (Active) |CC Value (Active) | - |
**Description**
This Midi message sends a Control Change message with a different Control Change message each time the switch is pressed down. Step once to send a CC message of with Number 1 andValue 1, and step again to send a CC message with Number 2 and Value 2.
 
**Example of Use**
You can control the Boost volume on the Strymon Timeline by sending CC message with Number = 23. The value range is between 0-60. Setting Value 1 = 0 and Value 2 = 60 will enable you to switch between a -3db and +3db boost.


## PC Toggle Hold
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |0 - 127           | -              | 0 - 127             | -              |1 - 16           |
| **Details**   |PC Number (Press)|-| PC Number (Release)| -| - |
**Description**
This Midi message sends a Program Change message with Number 1 when the switch is pressed and a different Program Change message with Number 2 when the switch is released. 
 
**Example of Use**
Momentarily switch to a different preset for a special setting and then quickly go back to the original preset when the switch is released.


## CC Toggle Hold
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |0 - 127           |0 - 127              | 0 - 127             | 0 - 127              |1 - 16           |
| **Details**   |CC Number (Press)|CC Value (Press)|CC Number (Release)|CC Value (Release)| - |
**Description**
This Midi message sends a Control Change message with Number 1 and Value 1 when the switch is down, and a different Control Change message with Number 2 and Value 2 when the switch is released. 
 
**Example of Use**
Quickly turn the delay mix on the Strymon Timeline down by stepping on the switch, and have the mix bank up when the switch is released. Set Number 1 and 2 = 14, Value 1 = 50 and Value 2 = 127.

## CC Hold Delay
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |0 - 127           |0 - 127              | 0 - 127             | 0 - 127              |1 - 16           |
| **Details**   |CC Number (Press)|CC Value (Press)|CC Number (Hold)|CC Value (Hold)| - |
**Description**
Sends a Midi Control Change message only if the switch is held down for more than 600ms. A CC Message of Number = Number 1 and Value = Value 1 will be sent out when the switch is pressed down. If held more more than 600ms, a CC message of Number = Number 2 and Value = Value 2 will be sent out.
 
**Example of Use**
This function is very useful when you want to assign one footswitch to switch banks, and then activate a preset once you have selected your desired bank just by holding down on the footswitch. Another cool use for this is to set your looper's play function to Number 1 and Value 1, and Stop function to Number 2 and Value 2. That way, you can have 2 useful functions in one preset. Just press the switch once if you need to play the loop, and hold it down when you want to stop the loop.


## Note On
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |0 - 127           |0 - 127         | -             | -              |1 - 16           |
| **Details**   |Note Value|Velocity| -             | -              | - |
**Description**
Sends a Midi Note On Message with the Note Value as Number and Velocity as Value 1.

## Note Off
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |0 - 127           |0 - 127         | -             | -              |1 - 16           |
| **Details**   |Note Value|Velocity| -             | -              | - |
**Description**
Sends a Midi Note Off Message with the Note Value as Number and Velocity as Value 1.

## Midi Clock Tap Tempo
| | Number1| Value1 |Number2| Value2| Channel |Comments|
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|:---:|
| **Values**   |0 - 127           |0 - 127         | -             | -              |-           |-|
| **Details**   |**x**|**y**| | -|-|Tempo = 100**x** + **y**
**Description**
Sends a Midi Clock signal to out from USB and 5 Pin Midi. Syncs your Midi Clock enabled devices to a common BPM. Tapping the switch once brings you to the Midi Clock menu, and immediately starts sending the clock sigals. You can set the set the BPM using the following formula:
 
BPM = (Number1 * 100) + Value1
 
This will be the BPM used on first tap. When in the Midi Clock menu, you can tap a new tempo and the Midi Clock signals will adjust to the new tempo simultaneously. When you are satisfied with the new tempo, you can either Exit the menu, or save the new tempo by holding down the Exit switch (Switch C). The LCD will indicate that the tempo is saved, before exiting the menu.
 

## Strymon Bank Up
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |-                |-              | -             | -              |1 - 16               |
| **Details**   |-|-| -| -|-
**Description**
Bank up on your Strymon Timeline, Möbius and Bigsky

## Strymon Bank Down
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |-                |-              | -             | -              |1 - 16               |
| **Details**   |-|-| -| -|-
**Description**
Bank down on your Strymon Timeline, Möbius and Bigsky

## PC Scroll Up
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |0 - 7           |0 - 1              | -             | -              |1 - 16           |
| **Details**   |Select slot number|1 = Increase<br>0 = No change| -| -|-
**Description**
Send PC messages with an incremental number. This message type allows you to scroll through presets on single or multiple devices at the same time. The MC6 contains an array which holds 8 numbers that you can select and scroll between 0 - 127. Use Number1 to select the number in the array based on its position, and use Value1 to determine whether to increase the number by 1. If Value1 is >0, the message will increase the selected number by 1. The number will be stored into memory and will be recalled when the device is restarted.

Simply put, if you want to scroll through a device, set Number1 = 0 and Value1 = 1. If you want to scroll through a second device with the same switch, set Number1 = 0 and Value1 = 0 for the next message.
 
**Example of Use**
To scroll through multiple devices, set Msg1 to have Number1 = 0 and Value1 = 1. Let's assume that the value at position 0 in the array is 0. Calling this message will increase the value to 1, and then send a PC#1 message. Pressing it again will send a PC#2 message. If you would like to control a second device, set Msg2 to have Number1 = 0 (so it is pointing to the same value as Msg1) and Value1 = 0 (so that you will not increase the value when Msg2 is called). Now, each time you press the switch, Msg1 and Msg2 will send the same PC message at their set channels.

Read more here about this message type here:
http://www.morningstarfx.com/single-post/2016/10/16/Using-the-PC-Scroll-Midi-Type


## PC Scroll Down
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |0 - 7           |0 - 1              | -             | -              |1 - 16           |
| **Details**   |Select slot number|1 = Decrease<br>0 = No change| -| -|-
**Description**
Similar to PC Scroll Up, but this Midi Type decreases the value instead.

## MC6 Bank Up
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |-      |-         | -        | -         |-             |
| **Details**   |-      |-         | -        | -         |-             |           |-               |
**Description**
This is useful if you need to bank up on the MC6 without having to step on two switches. You will be able to scroll up the banks if you hold down the switch. However, if you step once and release, you will need to wait for the bank to load before you are able to bank up again. If you want to have a dedicated bank up/down button in all the banks, you can copy this function and paste it to all banks by using the Copy All function (holding down the copy switch)

## MC6 Bank Down
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |-      |-         | -        | -         |-             |
| **Details**   |-      |-         | -        | -         |-             |    
**Description**
Similar to MC6 Bank Up function, but this banks down instead.

## Conditional Type
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |0 - 2           |0 - 3         | -             | -              |-           |
| **Details**   |-|-|-|-|-|
**Description**
This handy little function will help you extend your controller's functionalities. "Conditional Types" are basically conditional functions that can help you skip certain messages, or send certain messages, depending on how the switch is used. For example, you might want to send a Strymon Bank Up/Down type when the switch is pressed, and a Toggle/Bypass message when the switch is held down. This is possible by sending a Bank Up/Down message, and then adding a CC Hold Delay type to call the Active/Bypass on the Strymon when the switch is held down. However, what if you just want to call the Active/Bypass function without changing banks? This is where Conditionals come in.
 
Depending on the value of Number1:Value1, the Conditional will function differently. Misc Types like Delay uses Number2:Value2 as well.
 
|Type|Number1|Value1|Description|
|:---:|:---:|:---:|:---:|
Misc|0|0|Placeholder
Misc|0|1 |Delay the next message in milliseconds = (Number2 * 100) + Value2. (1000ms = 1 second). Max 2 seconds.
When Switch Released|1|0|Do nothing
When Switch Released|1|1|Send all the messages after this Conditional.
If switch is held down (600ms)|2|0|Do Nothing
If switch is held down (600ms)|2|1|Send the rest of the messages after this Conditional.<br>Else, skip everything.
If switch is held down (600ms)|2|2|Skip to the next Conditional Placeholder (0:0) and send the messages after that Placeholder.<br>Else, send the rest of the messages after this Conditional when the switch is released, up till the next Placeholder.
If switch is held down (600ms)|2|3|Skip to the next Conditional Placeholder (0:0) and send the messages after that Placeholder.<br>Else, send all the messages, ignoring all Placeholders, when the switch is released.
 
Going back to the example earlier, you could set Msg1 to be a "Skip to placeholder" Conditional (2:2), Msg 2 to be your Bank Up/Down message, Msg3 to be a Placeholder Conditional (0:0), and then Msg4 to be your CC message to Active/Bypass your Strymon. You can now Bank Up/Down with each switch press, and when you need to call the Active/Bypass function without changing banks, just hold the switch down and only the Active/Bypass message will be sent out.
 

## System Real Time
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |0 - 3           |-        | -             | -              |-           |
| **Details**   |Select System Msg Type|-| -| -|-|
**Description**
Sends different real time messages based on the value of Number 1.
 
|Number1|Description|
|:---:|:---:|
0| Send nothing
1|Start
2|Stop
3|Continue
 
## AxeFX Tuner
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |0 - 127           |0 - 127              | 0 - 127             | 0 - 127              |1 - 16           |
| **Details**   |CC Number (Tuner)|CC Value (Tuner Engage)|CC Number (Tuner)|CC Value (Tuner Disengage)|-|
**Description**
Calls and receives tuner information from the AxeFX.
 
Firstly, this function sends a CC Message of Number1:Value1 upon engagement (usually CC#15 Value 127). Set this message to activate your AxeFX Tuner function (Tuner is usually set of CC#15 value 127). The LCD will show that it is waiting for tuner information. Upon receving the SysEx tuner message from the AxeFX, the LCD will switch to tuning mode.
 
Press EXIT to send a CC message of Number2:Value2 to disengage your tuner (usually CC#15 Value 0).
 
Things to note
1. Turn off Midi Thru on your AxeFX.
2. Enable SysEx send on your AxeFX.
 
## Custom SysEx Messages
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |0 - 127           |0 - 127              | 0 - 127             | 0 - 127              |-           |
| **Details**   |First msg = Sysex Length, else Sysex Number|Sysex Number|Sysex Number|Sysex Number|-|-|
**Description**
Create your own custom SysEx messages for each preset. String together a SysEx array using the any of the Midi Msg in each preset by selecting this Midi Type. Parameters N1:V1 and N2:V2 will be used as bytes in the SysEx Array in the following order [N1, V1, N2, V2].

Set N1 in your first SysEx message to be the length of the message, and use the remaining parameters as part of your SysEx message. Adding the head (0xF0) and tail (0xF7) of the SysEx message is not required.

Hence, to send a SysEx array that looks like this: [240, 1, 2, 3, 4, 5, 6, 247], you will need to use any 2 Midi Msg in the preset. It should look like this:
 
Midi Msg 1: N1 = 6, V1 = 1, N2 = 2, V2 = 3, Midi Type = SysEx
Midi Msg 2: N1 = 4, V1 = 5, N2 = 6, V2 = 0, Midi Type = SysEx

## Midi Thru
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |0 - 1           |-        | -             | -              |-           |
| **Details**   |0=On<br>1=Off|-| -| -|-|-|
**Description**
Set the Midi Thru on the MC6 to On or Off. Use N1 = 0 to turn it [Off] and N1 = 1 to turn it [On]. Midi Thru is always set to [On] upon power up.

**Example of Use**
When you want certain presets to sync with Midi Clock sent from an external device through the MC6, and other presets not to sync with the external Midi Clock.

## Clear Toggle
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |0 - 127           |0 - 127              | 0 - 127             | 0 - 127              |-           |
| **Details**   |127 = Clear All, <br> else Preset Number| Preset Number| Preset Number| Preset Number|-|-|
**Description**
When you want your toggle presets to interact with each other in one bank, add this Midi Type into your preset. This preset will allow you to set the state to [Off] and turn off the blinking for selected or all other presets when a new preset is selected.

You can choose to set the state of all presets in the current bank to [Off] by setting N1 = 127.
 
Alternatively, you can clear only selected presets by setting the parameters N1, V1, N2 and V2 to indicate which preset you would like to clear. For example, to clear only Presets A, B, and D, you should set N1 = 1, V1 = 2, N2 = 4 and V2 = 0. When a parameter is set to 0, it will be ignored.

**Example of Use**
1. Preset [A] and [B] are set to PC Toggle. Currently, when both Switch [A] and [B] are pressed, both Preset names will blink and their states will be set to [On].
2. For Preset [A] to stop blinking and state set to [Off] after Switch [B] is pressed, add a [Clear Toggle] Midi Type to Preset [A] and [B], so that their states will be mutually exclusive and both Presets will not be at a [On] state at the same time. 

## Clear Toggle (v2.4)
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |0 - 127           |0 - 127              | 0 - 127             | 0 - 127              |-           |
| **Details**   |127 = Set All, <br> else Preset Number| Preset Number| Preset Number| Preset Number|-|-|

**Description**
Similar to Clear Toggle, but sets the preset(s) to active.

## Blink

| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |-           |-        | -             | -              |-               
| **Details**   |-       |-          | -             | -              |-               
**Description**
To set any Midi Type to have a blinking effect, add this [Blink] Midi Type to your preset to toggle between [Off] and [On] states.

## Set Bank
| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |0 - 127           |-        | -        | -           |-     |
| **Details**   |127 = Last used bank<br>else Bank Number|-| -| -|-|
**Description**
Jumps to different banks on the MC6, or return to the previous bank from where you jumped. Use N1 = 0 - 29 to switch to banks 1-30 on the MC6. Set N1 = 127 to go back to the previous bank.



## Select Expression Message (v2.4)
 | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |0 - 1           |0 - 8        | -             | -              |-           |
| **Details**   |Expression Input Number. <br>0 = Exp1<br>1 = Exp2|Select Exp Msg. 0 = Select All<br>Else Msg| -| -|-|

## Toggle Page (v2.4)

| | Number1| Value1 |Number2| Value2| Channel |
|:-----------:|:--------:|:--------:|:---------:| :----------:| :--------:|
| **Values**   |-           |-        | -             | -              |-               
| **Details**   |-       |-          | -             | -              |-      
