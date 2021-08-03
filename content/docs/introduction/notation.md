---
weight: 10
---

# Music Notation

Western music notation starts with staffs, clefs, and notes. Then it gets complicated.
For hundreds of years, people have been adding new symbols and annotations to music notation to better express
how the music is intended to sound. 

Dorico supports pretty much any notation you can imagine. Hundreds of notations are built in, 
and you can create your own if you need to. 
During playback, Dorico does an amazing job of keeping track of all the notations that apply to a particular note.
It boils them down into a pitch, a duration, a volume, and set of "playing techniques".
But what Dorico _needs_ to play a note is a series of MIDI events to send to a
[VST instrument](https://en.wikipedia.org/wiki/Virtual_Studio_Technology).

That's where expression maps come in. An expression map takes in all the information that Dorico has about a note
(pitch, duration, volume, and playing techniques) and maps it to a series of MIDI signals that Dorico then sends to
the VST instrument.
