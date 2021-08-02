---
title: VST Sounds Tab
weight: 2
---

## The VST Sounds tab

The VST tab is for entering VST sounds. 

![Example](/vst-tab.png)

### Base Sounds

This is where you enter the sounds you want to use from your VST instrument. 
To add a new sound, click the plus sign and fill in the blanks:

#### Name 

Give the sound a name that you'll recognize later. It will show up on the Assignment tab.

#### Start

The MIDI events to send to start the sound, separated by commas.
See [Specifying MIDI events](/docs/tool/vst-tab/#specifying-midi-events) for details of how to write MIDI events.

#### Stop events

These MIDI events are sent to stop the sound.
See [Specifying MIDI events]() for details of how to write MIDI events.

#### Dynamics

You can specify either velocity or a continuous controller to control velocity, and a range of velocities to use. 

##### Velocity

Just use the word "velocity", optionally followed by a range. Examples:

    velocity
    velocity 10:120

##### Continuous controller
Examples:

    CC3
    cc17 10:120


### Specifying MIDI events

#### MIDI Key Switch

A MIDI note number. Examples:

    KS3
    ks13
    ks 7

The default velocity is 127. If you need to change
that, you can include the velocity after an "=" sign. Examples:

    KS3=2
    ks13=125
    ks 7 = 13

#### Note

A keyboard note. Examples:

    C0
    d#2
    f 3

Middle C is by default **C4**. You can change that by opening the Options toggle at the top of the page and choosing
whatever middle C matches your VST.

As with key switches, the default velocity is 127. If you need to change
that, you can include the velocity after an "=" sign:

    C#3 = 64
    C0=120

#### CC setting

A continuous controller setting:

    CC3=17
    cc3 = 14

#### Program change

A program change:

    PC13
    pc 12

#### CC choice

Some VST instruments use a CC value to choose between several options.
E.g., CC3 might be used to make a six-way choice.
The first 1/6 of the range, approximately 0-21, picks the first choice;
the second 1/6 of the range, approximately 22-42, picks the second choice; and so on.

If there are more than two or three choices, it becomes error-prone to pick a value in the correct range.
Fugalist supports an alternative notation:

    CC3 = 4/6

will divide up the range into 6 parts and pick a value that falls in the middle of the 4th range.


### Add-on Techniques

TODO

{{< button relref="/composite-tab" >}}Next{{< /button >}}
