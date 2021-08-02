---
title: Introduction
type: docs
weight: 1
---

# What is an expression map?

_An expression map takes in the information that can be gleaned about a note from a musical score---pitch, duration,
relative volume, playing techniques, etc.---and produces MIDI signals to play the note more or less as
human would play it, but on a [VST instrument](https://en.wikipedia.org/wiki/Virtual_Studio_Technology)._

If that statement doesn't leave any questions in your mind, don't waste your time here: 
skip ahead to the [next section](/docs/tool).

Western music notation starts with staffs, clefs, and notes. Then it gets complicated.
For hundreds of years, people have been adding new symbols and annotations to music notation to better express
how the music is intended to sound. 

Dorico supports pretty much any notation you can imagine. Hundreds are built in, and you can create your own if you
need to. During playback, Dorico does an amazing job of keeping track of all the notations that apply to a particular note.
It boils them down into a pitch, a duration, a volume, and set of "playing techniques".
But what Dorico _needs_ to play a note is a series of MIDI signals to send to a
[VST instrument](https://en.wikipedia.org/wiki/Virtual_Studio_Technology).

That's where expression maps come in. An expression map takes in all the information that Dorico has about a note
(pitch, duration, volume, and playing techniques) and maps it to a series of MIDI signals that Dorico then sends to
the VST instrument.

# One note at a time

For each note in a score, Dorico computes the pitch, duration, volume, and
the set of playing techniques that are active. 

Dorico itself takes care of pitch and duration for the most part, so you usually don't need to worry too much about
those[^note-duration].

Dorico needs a _little_ help with the volume: basically, it needs to know whether volume is controlled by note
velocity or by a MIDI CC and---if it's controlled by a MIDI CC---which one. 

So main job of the expression map is to figure out what to do with the playing techniques. 
Dorico uses the set of active playing techniques for the note, plus (optionally) the note duration, 
to find an expression map entry. Then it reads from the expression map entry the following:

- **On events**: a sequence of MIDI events to send before the note is played
- **Off events**: a sequence of MIDI events to send after the note is played (rarely needed, in my experience)
- **Volume dynamic**: A specification of how to control the volume of the note. The volume of a VST instrument 
can be controlled either by using the note velocity, or by some continuous control (CC).
- **Length adjustment**: an adjustment to the note length (percentage). 
- **Tranpose**: an adjustment to the note pitch in case the library is in a different octave.

[^note-duration]: However an expression map can take the note duration into account when deciding what MIDI to output,
and can also change the pitch by transposing notes up or down by octaves.)

So, in a sense, an expression map is a very simple thing. It's just a big look-up table, with one row for each
combination of playing techniques. Once Dorico finds the right row, it reads the _on_ events, _off_ events, etc., and
uses them to play the note. 

# So what's the problem?

This all seems pretty straightforward: figure out which playing techniques to support. Then create a table with
one row for each combination of playing techniques. Assign on events, off events, etc., for each row. 

The problem is scale. 
Suppose you want to support
1. five note articulations (normal, staccato, staccatissimo, tenuto, and staccato tenuto), 
2. normal and legato note transitions
3. normal and marcato attack, and 
4. normal and non- vibrato
5. normal, pizzicato, sul tasto, and sul pont.

That's 15 playing techniques, which means

    2^15 = 32768

table entries if you allow _any_ combination. 

Luckily, the vast majority of combinations don't make any sense.
A note can't be marked both legato and non-legato at the 
same time, nor can it be marked both staccato and staccatissimo. 
So we can do much better by noticing that it only makes
sense to pick _one_ playing technique from each of the numbered sets. 
That leaves

    5 * 2 * 2 * 2 * 3 = 120

sensible combinations. Still quite a few, but more manageable.

# Tiny Example

To be concrete, suppose we want to support the following playing techniques: 

- Normal and tenuto lengths
- Normal and legato note connections
- Normal and pizzicato technique

Here's a complete table of sensible combinations, eight in all:

Length | Legato | Technique | on  | off  | vol | etc
------ | ------ | ----------| --------- | ---------- | -------------- | ---
Normal | Normal | Normal    |
Normal | Normal | Pizz      |
Normal | Legato | Normal    |
Normal | Legato | Pizz      |
Tenuto | Normal | Normal    | 
Tenuto | Normal | Pizz      | 
Tenuto | Legato | Normal    | 
Tenuto | Legato | Pizz      | 

What remains is to fill in the blanks: specify on events, off events, etc., for
each combination. The Fugalist expression-map tool is designed to do exactly that.

{{< button relref="/tool" class="justify-end" >}}Next{{< /button >}}
