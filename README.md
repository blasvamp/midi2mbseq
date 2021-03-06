# midi2mbseq
mid file to mbseq (Arturia Microbrute sequence) converter

http://music.mebitek.com/news/mid-file-mbseq-arturia-microbrute-sequence-converter-released

# features
* gui interface and batch mode
* generate mbseq file from file or from directory
* a long mid file will be split into 8 sequences 
* option to fill the sequence with pauses to the nearest 16 multiple of the sequence length
* option to fill the sequence with pauses to custom value
* option to fill the sequence with pauses to the max microbrute sequencer size (64)
* set custom sequence length

### polyphonic midi notes
For polyphonic midi file each step of the sequencer will be filled with the first note in the midi message (if you play a chord just the highest note will be chosen).
Quantize is suggested but not needed.

# releases
* windows https://github.com/mebitek/midi2mbseq/blob/master/releases/mid2mbseq.exe
* osx https://github.com/mebitek/midi2mbseq/blob/master/releases/mid2mbseq-0.3.1.dmg
* java https://github.com/mebitek/midi2mbseq/blob/master/releases/mid2mbseq-0.3.1.jar

### run java as
```
java -jar mid2mbseq-0.3.1.jar
```
to run in batch mode
```
java -jar mid2mbseq-0.3.1.jar -b -i midi_file.mid
```
output will be `midi_file.mbseq`
```
java -jar mid2mbseq-0.3.1.jar -b -d /home/user/midi_directory
```
output will be `midi_directory.mbseq`

* add `-f` to use full filler option
* add `-m` to use multiple 16 filler option
* add `-c value` to use the filler with custom value
* add `-l` to use set the sequence length
