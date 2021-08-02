---
title: Composite Sounds Tab
weight: 3
---

## The Composite Sounds Tab

The composite sounds tab provides support for 
- note-length conditions
- length adjustments
- octave transpositions

A composite sound can have multiple branches that depend on note length. Here is an example:

![Example](/composite-tab.png)

If you assign this composite sound (**Sustain**) to some combination of playing techniques then, 
when Dorico plays a note with those techniques, it will decide whether to use
a **staccato** sound or a **sustain** based the duration of the note.  

When you create a composite sound (by clicking **+**) a single branch is created. You can add other branches to
the composite sound by clicking **+** on the right.

### Name 

Give your composite sound a name. 

### Condition

The condition determines which branch of the composite sound to use for a particular note. In the example above,
the first branch is used if the note length (as computed by Dorico) is less than **short**.[^note-lengths] 
The second branch is used otherwise. That means that short notes will use your _staccato_ patch, and longer notes
use the _sustain_ patch.

[^note-lengths]: Dorico defines the following note lengths:
    - **very short** 0.1875 seconds, or a dotted 16th note at 120bpm
    - **short** 0.375 seconds, or a dotted 8th note at 120bpm
    - **medium** 0.75 seconds, or a dotted quarter note at 120bpm
    - **long** 1.5 seconds, or a dotted half note at 120bpm

Fugalist is pretty flexible about how to write conditions. Examples:

    NoteLength <= veryShort
    note length <= very short
    very short < note length AND note length < long
    short <= note length and noteLength < long

In addition, you can specify ranges as follows:

    short < note length <= long
    very short < NoteLength < long

Finally, you can have a single branch and leave the condition empty, which effectively means it's always true.
That's useful if you just want to adjust length or transpose for one of your VST sounds without paying
attention to note length.

**Caveat**: Fugalist checks the _syntax_ of your conditions and tells you if it finds a mistake. 
E.g., if you write

    shortt < note length

Fugalist will tell you that "shortt" isn't something it understands. But, currently at least, Fugalist doesn't 
make any attempt to determine whether your conditions actually make sense. For example, if one of your conditions is

    NoteLength < short and Notelength > long

Fugalist will happily put that in your expression map in spite of the fact that it can never actually be true.

### Length

Enter a percentage if you want to adjust the note length. 

### Transpose

Enter a number (positive or negative) to transpose up or down.

### VST Sound

Select the VST sound to use for this branch. In the example above, short notes are played with the **staccato**
sound and longer notes played with the **sustain** sound. 
Both of those are defined in the [VST sounds tab](/docs/tool/vst-tab).
