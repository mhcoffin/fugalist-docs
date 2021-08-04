---
weight: 20
title: How Dorico Uses an Expression Map
---

# How does Dorico use an expression map?

For each note in a score, Dorico computes the pitch, duration, volume, and
the set of playing techniques that are active.

Dorico itself takes care of pitch and duration for the most part, so you usually don't need to worry too much about
them. 

{{< hint info >}}
However, you can [adjust Dorico's durations](/docs/tool/composite-tab/fields/#length) if you need to.
{{< /hint >}}

Dorico needs a little help with the volume. Basically, it needs to know whether volume is controlled by note
velocity or by a MIDI continuous controller (CC) and---if it's controlled by a MIDI CC---which one. 
Once you tell it _how_ to control volume, Dorico does the rest.

So main job of the expression map is to specify what to do with the playing techniques.
Dorico uses the set of active playing techniques for the note, plus (optionally) the note duration,
to find an expression-map entry. Then it reads from the expression-map entry the following:

- **On events**: a sequence of MIDI events to send before the note is played
- **Off events**: a sequence of MIDI events to send after the note is played
- **Volume dynamic**: A specification of how to control the volume of the note. The volume of a VST instrument
  can be controlled either by using note velocity, or by some continuous controller (CC).
- **Length adjustment**: an adjustment to the note length (percentage).
- **Tranposition**: an adjustment to the note pitch in case the library is in a different octave.

So, in a sense, an expression map is a very simple thing. It's just a big look-up table, with one row for each
combination of playing techniques. Once Dorico finds the right row, it reads the _on_ events, _off_ events, etc., and
uses them to play the note. 
