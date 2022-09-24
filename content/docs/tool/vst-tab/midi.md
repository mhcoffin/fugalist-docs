---
weight: 4
title: MIDI Event Syntax
---

# Specifying MIDI Events

## MIDI Key Switch

A MIDI key switch can be specified either as a note number (0-127) or as a chromatic note plus an octave.

### MIDI Note Number

To specify a MIDI note number, just prefix the number with **KS**:

    KS3
    ks13
    ks 7

The default velocity is 127. If you need to specify a different velocity, you can specify the velocity 
after an "=" sign. Examples:

    KS3=2
    ks13=125
    ks 7 = 13

### Keyboard Note

A chromatic note with an octave number:

    C0
    d#2
    f 3

{{< hint info >}}
Middle C is by default **C4**. 
If your VST vendor has a different opinion, you can open the Options toggle at the top of the VST Sounds tab and choose
a different octave.
{{< /hint >}}

As with note numbers, the default velocity is 127. If you need to change
that, you can include the velocity after an "**=**" sign:

    C#3 = 64
    C0=120

## CC Values

To set a continuous controller to a particular value:

    CC3=17
    cc3 = 14

## CC Ranges

Some VST instruments use a continuous controller to choose between several options.
E.g., CC3 might be used to make a six-way choice.
The first 1/6 of the range, approximately 0-21, picks the first choice;
the second 1/6 of the range, approximately 22-42, picks the second choice; and so on.

If there are more than two or three choices, it becomes error-prone to pick a value in the correct range.
Fugalist supports an alternative notation:

    CC3 = 4/6

This will divide the range 0-127 into six parts and pick a value that falls in the middle of the fourth range.

## MIDI Program change

To enter a MIDI program change, prefix the program number with **PC**:

    PC13
    pc 12
