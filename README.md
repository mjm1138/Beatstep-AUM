# Beatstep-AUM
Preset for Arturia Beatstep (not pro) and AUM session template for controlling AUM with Beatstep

## Usage
You need:
* An Aurturia Beatstep (not a Beatstep pro)
* A computer with Arturia MIDI Control Center
* An iOS/iPadOS device running Kymatica AUM

The file AUMCC.beatstep is a preset file. It can be imported into Arturia MIDI Control Center and applied to a memory location on your Beatstep. I use location 16.

The file 8_Tracks_Audio_BS is an AUM session file (which is an Apple binary plist file). You can use plutil in macOS to examine the contents of the file. Place this file in your iCloud drive, and use the Files app to move it in to the AUM folder on your iOS/iPadOS device.

I suggest using the AUM session file as a template (i.e. immediately save it to a new name before beginning work). You should be able to remove unused audio tracks without affecting mapping, but if you add a track back, you'll have to manually re-map it in the "Midi Control" menu of AUM.

## What are the MIDI Maps?
You can examine the maps in detail in MIDI Control Center, but the basic gist is
* Big knob: Channel 16 CC 7 - mapped to the master channel volume in the AUM project
* Knobs 1-8: CC7 on Channels 1-8 respectively, to match the default AUM mapping for channel volume
* Knobs 9-16: CC10 on Channels 1-8 respectively, mapped to stereo pan for each track in AUM
* Pads 1-8: CC44-51 on Global Channel (16), for whatever use
* Pads 9-16: CC9 on Channels 1-8 respectively, mapped to channel mute for each track in AUM
* Global Channel is 16

## What's in the AUM session?
* 8 empty audio tracks with a post-fader stereo panner
* 2 midi tracks with 4 empty slots each
* 1 master audio track
* MIDI maps set up as described above

