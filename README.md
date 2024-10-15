# anything2midi

Code files for a workshop for building a MIDI controller, held on November 4th and 5th at MaM+a club in Zagreb.

## Links

Board Definitions: [Dasduino Board Definitions for Arduino IDE](https://github.com/SolderedElectronics/Dasduino-Board-Definitions-for-Arduino-IDE/raw/master/package_Dasduino_Boards_index.json)

LoopMIDI: [LoopMIDI by Tobias Erichsen](https://www.tobias-erichsen.de/software/loopmidi.html)

Hairless MIDI: [Hairless MIDI Serial Bridge](https://projectgus.github.io/hairless-midiserial/)

Surge XT: [Surge Synthesizer](https://surge-synthesizer.github.io/)

## Tutorial for Sending MIDI Notes

1. Connect the Arduino/Dasduino via USB to your computer.

2. Install the RBD Button and RBD Timer libraries, then open example 2 from this repository in the Arduino IDE.

3. Upload the example to the board. If the User button is on a different pin, change '0' in line 6 to the number of the corresponding pin.

4. Launch Hairless MIDI and LoopMIDI. In LoopMIDI, create a new port and connect it in Hairless MIDI so that the Arduino Serial sends to this port.

5. Open Surge XT and enable this virtual MIDI port in the options, the one created by LoopMIDI.

6. Try pressing the button to play.

## For Linux (Thanks to j3d1n4)

Instead of Hairless MIDI and LoopMIDI, use:
[Arch Linux Udev Loading New Rules Guide](https://wiki.archlinux.org/title/Udev#Loading_new_rules)
```bash
ttymidi | timidity -iA
```
(Start Timidity in "ALSA server mode" for Surge XT)
