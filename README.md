# MC6-Midi-Controller
Binary releases for the Morningstar Engineering Midi Controllers

Developmental Release: v2.4 Beta

__Switching Changes__
* Changed Edit Bank from Switch [C + F] to Switch [B + E]
* Changed Toggle Midi Editor from Switch [A + D] + [F] to Switch [D + C]
* Changed Toggle Midi Thru from Switch [A + D] + [C] to Switch [F + A]

__Additional Preset Switches__
* Switch [D + E] calls Preset G
* Switch [E + F] calls Preset H
* Switch [A + D] calls Preset I
* Switch [B + E] calls Preset J
* Switch [C + F] calls Preset K

Latest Release: v2.3

__Midi Types__
* Added SysEx Midi Type.
  * Users can now create their own custom SysEx message to send out via DIN5 Midi and USB Midi.
* Added Set Midi Thru Type
  * Users can now control the MC6 Midi Thru and turn it ON or OFF in a preset.
* Added Clear Toggle Type
  * This type resets all toggle keys for all presets in the current active bank, which will allow you to use the bank as a "Scene" or "Preset" select. 
* Added Blink Midi Type
  * Blink any preset by adding this Midi Type.
* MC6 Bank up and Bank down
  * Smoother bank changing using presets. No longer required to allow next bank to load before being able to change bank.
* CC Message
  * CC Continuous sending now enabled. Set N2 = 127 and V2 = 127 to continuously send CC#N1:V1 while switch is held down.
* Set Bank
  * Jump to a pre-determined bank, or bank to your previous bank.

__Midi Editor Mode__
* Toggle in and out of Midi Editor mode by pressing Switch [A + D] together, and then Switch [F]. Powering down and up is not required.
* Removed function to enter Midi Editor mode, where the user holds Switch [A] before powering up.

__DIN5-USB Mode__
* Rename to "Midi Thru".
* Toggle can be done by pressing Switch [A + D] together, and then Switch [C], or toggled from the Main Configuration menu.

__Preset Manager__
* Added implementation for the MC6 to work with the Morningstar Preset Manager to allow users to download and upload presets


__Bug Fixes__
* Midi Clock
  * Fixed issue where BPM reads the switch twice if the switch is held down for too long and released
* Factory Reset
  * Fixed issue where MC6 will do a Factory Reset when Switches D + F are held down for too long. Configuration menu now only loads when switches are released, and the Reset function is changed from Switch D to Switch E to prevent the user from accidentally doing a Factory Reset.
* Fixed usbMIDI thru bug

__Minor Changes__
* Renamed Midi Type "SysEx RT" to "System RT"

