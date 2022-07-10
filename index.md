## An experiment in Brain Control Interface as an Instrument

Originally designed as a PureData patch for performance installations, this is now growing into a full Brain Control Interface.

## Moving from Pd to Max
PureData had amazing potential and powerful audio visual controls, but with the discontinuation of PureData-Extended and the PureData-Vanilla requiring constant maintanence of libraries, I decided to move this project into Max. I am still an avid Pd user, but having to stop and update libraries everytime I needed to use this system for a performance was just simply no longer feasible

Even Max is too simplistic for the actual BCI.  The Max Patches are for audio and visual control, but to improve the reliability of processing of EEG data I had to build the actual interface in Python.

## OpenBCI
OpenBCI is an open source hardware that is the cutting edge of BCI on the market.  They produce the best commercial EEG platform that I have found with a complete open source mindset to allow developers to go into the Hardware and the software and develop their own implementation.

### Ganglion
The current system uses a 4 channel Ganglion.  This allows 2 channels in the visual cortex and 2 channels either on the motor cortex or on the frontal cortex.  The frontal cortex provides also eye movement information and is easier to implement using a simple headband.

The motor cortex requires a headset and for that I currently use the Mk IV.  This is complete overkill for 4 channels, but I am hoping to move to using the Cyton and Daisy soon.

## Python and SciKitLearn
In order to properly deal with real time EEG data, it was necessary to build a CNN model to learn the basic reactions to stimulous.  The current iteration is based on a 4 quadrant system and recognistion of stimulous in one of the quadrants.  This is hopefully used to allow participants to think about moving a mouse to the desired location and recognise where they are directing the mouse.  This is a super simple proof of concept that we hope to expand upon, but for now we are just 
