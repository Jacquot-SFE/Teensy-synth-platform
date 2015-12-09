# Teensy-based Synthesizer Development Platform Board Spec

## Objective

To build a carrier board for the Teensy 3.2 with features that allow it to be used as a platform to develop a synthesizer.

The immediate goal is to have a more usable system for prototyping.  It will contain the audio and MIDI core of a synth/drum machine/FX processor, with a reasonably considered set of interfaces for adding a control panel. 

This board might be a mezzanine device itself, on a larger board that connects pots, LEDs, switches and displays.

Eventually, it might grow into one or more condensed realizations of actual synthesizers or other audio device.  

### Features

1. Mezzanine location for a Teensy 3.2, with all of the extra underside & off-grid pads broken out.
	2. See FrankB's "connectorboard" from OSHPark for one concept using castellated vias. 
2. MIDI in-out-thru circuitry with 5-pin DIN connectors
3. Audio Codec or AD/DA
	1. Preferably a 2-input, 4 (or more) output chip like [these from TI](http://www.ti.com/lsds/ti/audio-ic/audio-dac-product.page#p1339=2 / 4)
	2. Alternatively, individual AD and DA chips.  The [TI PCM5100A](http://www.ti.com/product/PCM5100A) is cheap and chrreful.
4. (debatable) locations for SPI memory and/or SD card, similar to the audio board
5. Power Supply with more available current than the Teensy itself offers, possibly also higher voltage rails for audio interfaces (+/- 12V?).
6. Audio I/O on 1/4" TRS connectors
	7. Possibly with line-receiver/driver ICs for more standard interface levels,   Such as THAT 1646/THAT 1206.
	8. Altenatively, just using opamp diff receivers and drivers...
7. Broken out interfaces for expansion & user interface:
	8. 	Analog pins - including AGND and AREF
	9. 	Digital pins
	9. 	I2C
	10. SPI
	9. 	(Is there a need to make the teensy programming button available?)




### Form Factor

Roughly the size of an index card: ~3" x 5".

All external connectors aligned on the same edge:

* Teensy USB programming port
* MIDI
* Audio

Other connections for additional hardware for user-interface are available as 0.1" header pads on one of the other edges.

## Contingencies

Multichannel I2S ("PCM or DSP mode") from the Teensy isn't totally proven, but "[Theoretically Possible](https://forum.pjrc.com/threads/29373-Bit-bang-multiple-I2S-inputs-simultaneously?p=79606#post79606)".  Apparently the on-chip peripheral supports it, but the default software doesn't...yet?


## References

* [Teensy Audio Shield](http://www.pjrc.com/store/teensy3_audio.html) product page
* The audio shield uses the NXP [SGTL5000 codec](http://www.nxp.com/products/interface-and-connectivity/interface-and-system-management/switch-monitoring-ics/ultra-low-power-audio-codec:SGTL5000) 