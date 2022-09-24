---
weight: 6
title: VSL Synchron Instruments
---

# Working with VSL Synchron instruments.

I use [Vienna Symphonic Library](https://www.vsl.co.at/en) (VSL) Synchron instruments quite a bit,
so I've added some special features to deal with these instruments.

Many VSL Synchron instruments have a huge number of articulations, which can make it extremely tedious and error-prone
to enter all the key-switches, CC settings, etc. Luckily, the Synchron player has a way to
copy and paste the Synchron Tree View in machine-readable form. This allows you to save the Tree View to a file, which
you can then load into
Fugalist to get a complete set of VST sounds, complete with all the MIDI controls. 
This takes a lot of the pain out of creating expression maps for Synchron instruments.

Here's how you do it.

### In your Synchron player:

- Go to a loaded Synchron instrument. Customize it however you like.
  Make a note of how you set the Dimension Controls and how you control dynamics.
- Right click in a blank area of the Synchron Tree View to pop up the menu. Click on "Copy Root Slot". 
  This puts a bunch of text into the clipboard.
- Create a text file in your editor of choice and paste the clipboard. Save the file. 

{{< hint >}}
On a Mac, if you are comfortable with using the command line, 
you can create this file quickly without an editor using the 
command

    clippaste > filename

{{< /hint >}}


### Now back to Fugalist:

- At the top of the VST Sounds Tab in Fugalist, open the Options drop-down.
- Set the Default Dynamic to whatever CC you are using in the Synchron player.
- For each Dimension Control that you are using, click on the appropriate control and choose a CC number (or
  "speed").
- Import the file you created earlier by pasting the Root Slot.

The VST tab should be filled in with a complete list of all the sounds in the Synchron Tree View,
along with key-switches, CC settings, etc. You can, of course, edit this: delete any sounds you don't
intend to use and change names if you find them cumbersome.

{{< hint danger >}}
After import, if the VST tab contains any errors, it probably means you forgot to define all the Dimension Controls
that your instrument uses. If this happens, you can just define them and re-import the file.
{{< /hint >}}
