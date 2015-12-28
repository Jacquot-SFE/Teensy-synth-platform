# Teensy-Boom

## Teensy Audio based drum machine.

## Objective

To build a board that attaches to a Teensy 3.2, adding features to make a simple drum machine.

Secondarily, to make a board that could be used for other teensy-audio development efforts.

The goal is a modest and practicable drum machine, not a signfiicantly complex one.  It would be like a TR606, rather than a TR808.

Target price would be ~$100 for the Teensy 3.2 and this board...possibly including a case or front panel for another ~$25.

## Features

1. Mezzanine location for a Teensy 3.2, with all of the extra underside & off-grid pads broken out.
	2. See FrankB's "connectorboard" from OSHPark for one concept using castellated vias. 
2. MIDI in-out (thru?) circuitry with 5-pin DIN connectors
3. Audio DAC (or Codec)
	1. 2 outputs minimum,
	2. Preferably 4 (or more)
		1. _we have yet to prove the concept of DSP/TDM-mode on the I2S hardware_
	3. Audio I/O on 1/4" TRS connectors
	4. (no inputs?)
4. (debatable) locations for SPI memory and/or SD card, similar to the audio board
5. Power Supply with more available current than the Teensy itself offers.
6. Headphone output (possibly as a DAC feature)


## Form Factor

Large enough to allow the controls and alyout described below.  Initial guess is ~4" x 6".

Preferably in a form that allows the controls to meet a panel at a single elevation.

This might be a 2-sided layout - the pots and buttons on one side, with connectors and SMT
components on the reverse.

### Control Layout

Initial intent is to look something like a classic TR-family drum machine.

* 16 pattern buttons across bottom edge 
	* (thinking 6mm tact switches)
* 16 pattern LEDs above them 
	* (thinking 3mm PTH LEDs)
* Above that, vertical columns of controls, per voice (listed below).
	* (thinking pots with self-contained knobs...SFE little blue ones, or Alps/Alpha make some options)
* Master controls on the right-hand side of the panel
	* play/stop button (w/ LED)
	* Tempo
	* mode switches (w/ LEDs as needed)
	
### Connector layout 

All external connectors aligned on the same edge:

* Teensy USB programming port
* MIDI I/O (T?)
* Audio
* headphone
* Power supply jack

## Hardware Connections

* 24 buttons and 24 LEDs all connected using chains of shift-registers, via SPI
	* _would this complcate SD or outpuard flash interfacing?  How does Teensy handle !CS?_
* The 14 pots would use the 14 unused analog pins on the Teensy 3.2.
* MIDI would be one of the serial ports.
* If we had enough extra digital pins, some extra features on the tempo control might be cool
	* Rotary encoder w/ push-to-tap tempo option?
	* 7-seg tempo display

The allocation of the 14 ADC inputs is proposed as:

* Global controls
	* tempo control
	* master volume
* Kick drum
	* pitch
	* bend depth
	* length
* Snare drum
	* pitch
	* noise/tone crossfade
	* length
* Toms - 3 modules, but with ganged controls (they'd be a major triad above the base "pitch")
	* pitch
	* harmony-pitch
	* length
* Cymbal
	* tone
	* length
* Hihat
	* Open length

The "length" control on each channnel would be aligned, so all of the "lengths" are in a row, from left to right.
	
## Software Considerations

A mockup of the DSP portion of this runs on a teensy 3.2 at 72 MHZ, using ~40% of the processor.

This is with non-optimized modules for much of the processing.

### Modes

(There are 8 proposed buttons outside of the 16 pattern buttons -- what do they do?)

* sequence start/stop
* pattern-edit - the 16 enter notes into the active sequence.
* pattern-play - the 16 select the next sequence to play, possibly using an 8*8 banking scheme for 64 patterns for easy recall?
* voice select - in pattern edit, hold this, then use the 16 to select which voice is being programmmed.
* voice mute - while playing, hold this, then use the 16 to prevent a voice from triggering

leaving 3 for expansion...potential uses:

* deeper config - MIDI channel, synch mode, swing/flam
* another layer of pattern/bank switching
* a "save" switch (like x0xbox)
* I'm sure i'm forgetting something necessary...

## References

* [Teensy Audio Shield](http://www.pjrc.com/store/teensy3_audio.html) product page
* The audio shield uses the NXP [SGTL5000 codec](http://www.nxp.com/products/interface-and-connectivity/interface-and-system-management/switch-monitoring-ics/ultra-low-power-audio-codec:SGTL5000) 