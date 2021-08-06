---
title: Body
weight: 2
---

# Assignment Tab Body

The body of the tab is just a bunch of rows, one for each combination of the playing techniques.
If you add or delete playing techniques, or rearrange the grouping, the rows of the table body will change
to reflect that.


Here is one row:

![rows](/assignment-row.png)

The first five columns represent a particular combination of playing techniques.
It will apply to any note where the active playing techniques are exactly _non vibrato_ and _marcato_.

{{< hint info >}}
Remember that _Normal_ means the absence of any explicitly specified playing technique from the same group.
{{< /hint >}}

The last column is a drop-down where you can pick any of the VST sounds or composite sounds
that you've defined earlier.
In this case, the VST contains a _marcato non-vibrato_ patch, so that is assigned.
The result will be that Dorico will play any note labeled with exactly _non vibrato_ and _marcato_ using the **start** and
**stop** MIDI events specified for the _marcato non-vibrato_ sound.

One (tedious) way to create an expression map would be to go through every row of the table,
examine the playing techniques, select a VST or Composite sound, and assign it.
But frequently we can do better than that.
