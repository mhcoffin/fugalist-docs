---
weight: 2
title: Base Sounds
---

# Base Sounds

This is where you enter the sounds you want to use from your VST instrument.
To add a new sound, click the **+** sign and fill in the blanks.
Here's one example row:

![example-row](/vst-sound-row.png)

## Name

Give the sound a name that you'll recognize later. I tend to use lower-case names for base sounds and
upper-case names for Composite sounds, but that's up to you.

## Start

Add the MIDI events to send to start the sound, separated by commas.
See [Specifying MIDI events](/docs/tool/vst-tab/midi) for details of how to write MIDI events.

## Stop events

(You quite likely don't need to use this field at all.)
These MIDI events are sent to stop the sound.
See [Specifying MIDI events](/docs/tool/vst-tab/midi) for details of how to write MIDI events.

## Dynamics

You can specify either MIDI note velocity or a MIDI continuous controller (CC) to control velocity.

{{< hint >}}
If all or most of the sounds of your VST instrument use the same dynamics control,
you can save some time and effort by opening the Options dropdown and specifying the Default Dynamics Control.
If you set this, it will apply to all sounds unless you explicitly override it with something else.
{{< /hint >}}

#### Velocity

Just use the word "velocity", optionally followed by an range. Examples:

    velocity
    velocity 10:120

#### Continuous controller

Examples:

    CC3
    cc17 10:120

If you leave out the range, it defaults to the full range (0:127).
