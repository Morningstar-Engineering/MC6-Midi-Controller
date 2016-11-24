#MC6 Midi Types Reference
<p>
  Each preset contains 8 messages and sends them out in chronological order from message 1 to message 8.
  Each Midi Type consists of 6 different parameters: <b>Type, Number, Value 1, Value 2 and Channel</b>.
</p>
<p>
  Depending on the Midi Type you choose for each message, the numbers and values will be used differently.
</p>

##Range of valid values per Midi Type
| Midi Type        | Number 1         | Value 1        |Number 2        | Value 2         | Channel         |
|:----------------:|:----------------:|:--------------:|:--------------:| :--------------:| :--------------:|
| Empty Message    |-                |-              | -             | -              |-               |
| Program Change   |0 - 127           |-              | -             | -              |1 - 16           |
| Control Change   |0 - 127           |0 - 127         | -             | -              |1 - 16           |
| Program Change Toggle   |0 - 127           |-              | 0 - 127             | -              |1 - 16           |
| Control Change Toggle   |0 - 127           |0 - 127              | 0 - 127             | 0 - 127              |1 - 16           |
| Program Change Toggle Hold   |0 - 127           | -              | 0 - 127             | -              |1 - 16           |
| Control Change Toggle Hold   |0 - 127           |0 - 127              | 0 - 127             | 0 - 127              |1 - 16           |
| Control Change Hold Delay   |0 - 127           |0 - 127              | 0 - 127             | 0 - 127              |1 - 16           |
| Note On   |0 - 127           |0 - 127         | -             | -              |1 - 16           |
| Note Off   |0 - 127           |0 - 127         | -             | -              |1 - 16           |
| Midi clock Tap Tempo   |0 - 127           |0 - 127         | -             | -              |-           |
| Strymon Bank Up    |-                |-              | -             | -              |1 - 16               |
| Strymon Bank Down    |-                |-              | -             | -              |1 - 16               |
| PC Scroll Up   |0 - 7           |0 - 1              | -             | -              |1 - 16           |
| PC Scroll Down   |0 - 7           |0 - 1              | -             | -              |1 - 16           |
| MC6 Bank Up    |-                |-              | -             | -              |-               |
| MC6 Bank Down    |-                |-              | -             | -              |-               |
| Conditional Type   |0 - 127           |0 - 127         | -             | -              |-           |
| System Real Time   | 0 - 3           |-        | -             | -              |-           |
| AxeFX Tuner   |0 - 127           |0 - 127              | 0 - 127             | 0 - 127              |1 - 16           |
| Custom Sysex   |0 - 127           |0 - 127              | 0 - 127             | 0 - 127              |-           |
| Midi Thru   | 0 - 1           |-        | -             | -              |-           |
| Clear Toggle   |0 - 127           |0 - 127              | 0 - 127             | 0 - 127              |-           |
| Set Toggle   |0 - 127           |0 - 127              | 0 - 127             | 0 - 127              |-           |
| Blink    |-                |-              | -             | -              |-               |
| Set Bank   | 0 - 127           |-        | -             | -              |-           |
| Select Expression Message   | 0 - 1           |0 - 8        | -             | -              |-           |
| Toggle Page    |-                |-              | -             | -              |-               |

---
##Details

| Midi Type        | Number 1         | Value 1        |Number 2        | Value 2         | Channel         | Comments|
|:----------------:|:----------------:|:--------------:|:--------------:| :--------------:| :--------------:|:-------:|
| Empty Message    | - | - | - | - | - | - |
| Program Change   |PC Number|-| -| -|Channel| - |
| Control Change   |CC Number|CC Value| -| -|Channel| - |
| Program Change Toggle   |PC Number (Inactive) | - | PC Number (Active) | - |Channel | - |
| Control Change Toggle   |CC Number (Inactive) |CC Value (Inactive) |CC Number (Active) |CC Value (Active) | Channel | - |
| Program Change Toggle Hold   |PC Number (Press)|-| PC Number (Release)| -|1 - 16| - |
| Control Change Toggle Hold   |CC Number (Press)|CC Value (Press)|CC Number (Release)|CC Value (Release)|Channel| - |
| Control Change Hold Delay   |CC Number (Press)|CC Value (Press)|CC Number (Hold)|CC Value (Hold)|Channel| - |
| Note On   |Note Value|Velocity| -             | -              |Channel| - |
| Note Off   |Note Value|Velocity| -             | -              |Channel| - |
| Midi clock Tap Tempo   |**x**|**y**| -| -|-|Tempo = 100**x** + **y**
| Strymon Bank Up    |-|-| -| -|Channel|-|
| Strymon Bank Down     |-|-| -| -|Channel|-|
| PC Scroll Up   |Select slot number|1 = Increase. 0 = No change| -| -|Channel|-|
| PC Scroll Down   |Select slot number|1 = Decrease. 0 = No change| -| -|Channel|-|
| MC6 Bank Up    |-|-| -| -|-|-|
| MC6 Bank Down   |-|-| -| -|-|-|
| Conditional Type   |Refer|Refer| -| -|-|
| System Real Time   |Select System Msg Type|-| -| -|-|-|
| AxeFX Tuner   |CC Nummber for Tuner|Cc Value for Tuner Engage|CC Number for Tuner|CC Value for Tuner Disengage|Channel|-|
| Custom Sysex   |First msg = Sysex Length, else Sysex Number|Sysex Number|Sysex Number|Sysex Number|-|-|
| Midi Thru   |0=On, 1=Off|-| -| -|-|-|
| Clear Toggle   |127 = Clear All, else Preset Number| Preset Number| Preset Number| Preset Number|-|-|
| Set Toggle   |127 = Set All, else Preset Number| Preset Number| Preset Number| Preset Number|-|-|
| Blink    |-|-| -| -|-|-|
| Set Bank   |127 = Last used bank, else Bank Number|-| -| -|-|-|
| Select Expression Message   |Expression Input Number (1 or 2)|Select Exp Message | -| -|-|-|
| Toggle Page    |-|-| -| -|-|-|
---

##Type: Empty Message

<p>No data will be sent out.</p>
