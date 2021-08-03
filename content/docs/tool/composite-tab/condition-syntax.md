---
weight: 20
---

# How to Write Conditions

Fugalist is pretty flexible about how to write conditions.
You can use comparison operators to combine the actual note length (_NoteLength_) and Dorico's predefined note lengths.

Examples of simple comparisons:

    NoteLength <= veryShort
    note length <= very short
    very short < note length


{{< hint info >}}
Dorico's predefined note lengths:
- **very short** 0.1875 seconds, or a dotted 16th note at 120bpm
- **short** 0.375 seconds, or a dotted 8th note at 120bpm
- **medium** 0.75 seconds, or a dotted quarter note at 120bpm
- **long** 1.5 seconds, or a dotted half note at 120bpm
{{< /hint >}}

{{< hint info >}}
Comparison operators:
- **<=**
- **<**
- **>=**
- **>**
- **==**
- **!=**
{{< /hint >}}

You can combine simple comparisons with **and**. Examples:

    NoteLength > short and NoteLength < long
    very short < note length AND note length < long

Note-length ranges arise frequently; Fugalist provides a short-cut. The following two examples are equivalent:

    short < note length <= long
    short < NoteLength AND note length <= long


{{< hint warning >}}
Fugalist checks the syntax of your conditions, but it doesn't try to ensure that they make sense.

If you write

    shortt < note length

Fugalist will tell you that "shortt" isn't something it understands. 

But (currently at least) Fugalist doesn't
make any attempt to determine whether your conditions actually make sense. For example, if one of your conditions is

    NoteLength < short and Notelength > long

Fugalist will happily put that in your expression map in spite of the fact that it can never actually be true.
{{< /hint >}}

## Empty Condition

An empty condition is always **true**.
That's useful if you just want to adjust length or octave transposition for one of your VST sounds without paying
attention to note length.
