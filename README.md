# sidplay5
Sidplay for macOS

Since it seems that Sidplay 4.2 (http://www.sidmusic.org/sidplay/mac/) is no longer developed I decided to update the source and provide binaries for Intel and Apple Silicon. 

# asid support
Implementation of the asid midi protocol as a sound device in sidplay.
Adapted code from Sidplay4, implemented by Thorsten Klose on 15/10/09.
Adapted for Sidplay5 by Rio Rattenrudel.

The ASID protocol transmits MIDI data in real time, which is sent to hardware (such as therapsid, midibox sid, sidstation) that can play or even remix (applies to therapsid) sid tunes. This would be a good resource for people who own such hardware in use with a Mac as Intel/Apple Silicon build. 

It still needs [midi_patchbay](https://github.com/rio-rattenrudel/midi_patchbay/tree/master) to map ASID to your Midi equip!

* compile/start midi_patchbay
* compile/start Sidplay5 (asid)
* configure midi_patchbay with the MIDI input as ASID OUT and set the MIDI output to your MIDI interface
* power on your SID device and play sid tunes in Sidplay5 (emulator and data transfer run simultaneously)

# implemented changes
* 64 Bit binary, runs on macOS 10.9 or higher
* supports Intel and Apple Silicon
* code compiles now on latest Xcode
* auto-update feature disabled (for now)
* supports new song length database format
* expanded toolbar (old Mac OS X look&feel)
* SIDBlaster USB support (still not complete, digi songs will have issues)
* uses now libsidplayerfp

# still need to fix
* Xcode still complains about missing UI constraints and OpenGL
* info window still shows misplaced visual objects (minor)
* ~~starting with macOS 11, the toolbar height is smaller and the track info is cut off, stepping through subtunes is now a little bit tricky~~

