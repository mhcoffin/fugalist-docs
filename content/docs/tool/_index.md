---
title: Expression-map Builder
type: docs
weight: 2
---


# Fugalist expression-map builder

The Fugalist expression-map builder is an on-line tool for creating expression maps.
The intent is to simplify and streamline expression-map creation.

Fugalist stores your data in the cloud, so to use it, you have to be on-line and
signed in to Fugalist.

The builder consists of four tabs to deal with different aspects of building an expression map:

- The **Overview tab** is where you enter basic high-level metadata such as the expression-map name, instrument,
  VST library vendor, audio snippets, etc.

- The **VST Sounds** tab is where you enter the VST sounds you want to use from your sample library.
  For each sound you want to use, you provide a name of your choosing, the on- and off-events, and the volume dynamic.

- The **Composite sounds tab** deals with note-length conditions, length factors, and transpositions.
  For many sample libraries, you can skip this tab entirely.

- The **Assignment Tab** is a fancy version of the table described in the
  [previous section](/docs/intro/#tiny-example). Using this tab, you can specify which techniques you
  weant to support and how to group them.
  Then, for each row, you can assign a sound either from the VST Sounds tab or the Composite sounds tab.

  You can make sound assignments one row at a time, or you can select many rows at once (using technique filters)
  and assign a sound to all those rows.

The next sections go into more detail on each tab. 

{{< button relref="/overview-tab" class="justify-end" >}}Next{{< /button >}}
