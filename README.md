# PureData_Workshop
This repository contains all the materials you'll need for the NUSOUND PureData Workshop.
All patches were made using pd version 0.48.1.
DOWNLOAD PURE DATA: https://puredata.info/downloads/pure-data

There are 3 "stages" to this project, represented by 3 Pure Data Projects.
Stage 1 uses only a single `.pd` file, while stages 2 and 3 use multiple files (hence the folders).
Each stage has two versions: a "ref" version for reference, and a "diy" version.
The reference versions are completely finished while the diy versions have all the blocks
but still need all the connections to be made. This gives you three choices:
* Create your own project and build everything from scratch
* Open the diy files and fill in the connections
* Just use the reference projects and have fun playing the synths

Either way, the reference files are there to show you what the finished patch should look like.

Here's a brief summary of each stage:

## Stage 1
* Monophonic (one note at a time) sawtooth synth with a volume slider
* Uses basic MIDI processing and waveform generation (see MIDI setup instructions below)

## Stage 2
* Sawtooth synth with 8-voice polyphony and an ADSR envelope
* Uses abstraction (multiple files) to make life easier
* Send and receive utilities are used to pass signals between files
* Files are as follows:
	* main.pd: serves as the highest-level file that calls the others to generate notes
	* note.pd: generates tones based on the values passed to it by main.pd
	* adsr.pd: generates an envelope that modulates the dynamics of each note
## Stage 3
* Sawtooth synth with 8-voice polyphony, ADSR envelope, and a parameter-controlled filter
* Builds upon skills learned in stage 2
* filter.pd adjusts the frequency content of each note according to its four parameters:
	* Start: starting frequency
	* End: ending frequency
	* Time: time it takes to move from Start to End
	* Q: the q factor of the filter (try playing with the value to figure out what it does before googling it!)

## MIDI SETUP
* We can help you setup MIDI control, but here's a useful link if you want to do it yourself:
http://write.flossmanuals.net/pure-data/using-midi/

Every file has comments to help you understand the functionality of each block and what's going on.
Feel free to download the patches and remix them!
Possible add-ons include:
* Using other waveforms like cos or sin in note.pd
* Changing the filter type or adding more filters
* Adding a "harmony" section 
