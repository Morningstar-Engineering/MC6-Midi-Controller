#MC6 Midi Types Reference
<p>
  Each preset contains 8 messages and sends them out in chronological order from message 1 to message 8.
  Each Midi Type consists of 6 different parameters: <b>Type, Number, Value 1, Value 2 and Channel</b>.
</p>
<p>
  Depending on the Midi Type you choose for each message, the numbers and values will be used differently.
</p>

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
| PC Scroll Up   |0 - 7           |0 - 127              | -             | -              |1 - 16           |
| PC Scroll Down   |0 - 7           |0 - 127              | -             | -              |1 - 16           |
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

## Type: Empty Message

<p>No data will be sent out.</p>
