---
weight: 2
title: Base Sounds
---
# Base Sounds

This is where you enter the sounds you want to use from your VST instrument.
To add a new sound, click the **+** sign and fill in the blanks:

## Name

Give the sound a name that you'll recognize later. It will show up on the Assignment tab.

## Start

Add the MIDI events to send to start the sound, separated by commas.
See [Specifying MIDI events](/docs/tool/vst-tab/midi) for details of how to write MIDI events.

## Stop events

These MIDI events are sent to stop the sound.
See [Specifying MIDI events]() for details of how to write MIDI events.

## Dynamics

You can specify either note velocity or a continuous controller (CC) to control velocity:

#### Velocity

Just use the word "velocity", optionally followed by an optional range. Examples:

    velocity
    velocity 10:120

#### Continuous controller
Examples:

    CC3
    cc17 10:120
