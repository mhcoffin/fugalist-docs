---
weight: 3
---

# Add-on Techniques

Sometimes the planets align: your VST instrument will have a control that is

- independent of all the others, and 
- corresponds exactly to a Dorico playing technique. 

If this happens, you're in luck.

For example, you may find a VST instrument that uses CC3 to control attack.
Low values mean gentle attack, high values mean _marcato_ attack. Regardless of what else
is going on, CC3 controls note attack. 

You win. You can define an Add-On:

![add-on](/add-ons.png)

Select the Dorico playing technique (Marcato) from the dropdown. 
Then add the MIDI controls that will turn the effects on
and off. 
Dorico will set CC3 to 127 before playing a marcato note, and set it back to 64 for non-marcato notes. It
will do that no matter what else is going on.

The beauty of this is that _marcato_ is now taken care of once and for all. When you get to the sound-assignment tab, 
you can just delete the **Attack** axis, which cuts the size of the expression map in half and saves hassle, too.
