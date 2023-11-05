# anything2midi

Radionica izrade MIDI kontrolera, održano 4. i 5. 11. u klubu MaM+a u Zagrebu.

## Linkovi

Board Definitioni: https://github.com/SolderedElectronics/Dasduino-Board-Definitions-for-Arduino-IDE/raw/master/package_Dasduino_Boards_index.json

Loopmidi: https://www.tobias-erichsen.de/software/loopmidi.html

Hairless Midi: https://projectgus.github.io/hairless-midiserial/

SurgeXT: https://surge-synthesizer.github.io/

## Tutorial za slanje MIDI nota

1. Spoji Arduino/Dasduino putem USB-a na komp

2. Instaliraj RBD Button i RBD timer biblioteke i otvori example 2 iz ovog repozitorija u Arduino IDEu

3. Uploadaj example na pločicu, ako je User tipka na nekom drugom pinu, promjeni '0' iz linije 6 u broj tog pina

4. Upali programe Hairless MIDI i Loopmidi, na loopmidiju napravi novi port i spoji na hairless MIDIju da Serial od Arduina ide na taj port

5. Otvori Surge XT i u opcijama upali taj virtualni midi port koji je napraivo loopmidi

6. Probaj stisnuti tipku i svirati

## Za Linux (tnx j3d1n4)

https://wiki.archlinux.org/title/Udev#Loading_new_rules
umjesto hairless midi i loopMIDI:
ttymidi | timidity -iA
(dići timidity kao "ALSA server mode" za surge-xt)
