---
title: The Assignment Tab
weight: 4
---

## The Assignment Tab

The assignment is basically a fancy version of the [tiny example](/docs/intro/#tiny-example) shown earlier.
Here's an example:

![Example](/assign-tab.png)

The actual table is longer than that (40 lines), I've truncated it.

### The Header

The header shows all the playing techniques that this expression map supports, and how they are grouped. Each 
column is called an _axis_.

- The first axis (**Length**) consists of the Dorico playing techniques that indicate note duration:
_Normal_, _Staccato_, _Staccatissimo_, _Tenuto_, 
and _Staccato-tenuto_. _Normal_ means a lack of any other notation, so a note **not** marked _Staccato_, _Staccatissimo_,
_Tenuto_, or _Staccato-tenuto_ is automatically _Normal_.

- The second axis (**Legato**) consists of _Normal_ and _Legato_. Again, the absence of a _Legato_ indication means
_Normal_.

- The third axis (**Vibrato**) consists of _Normal_ and _Non vibrato_.

- The fourth axis (**Attack**) consists of _Normal_ and _Marcato_. 

- Finally, **Technique**, which contains only _Normal_ for now. 

The last column of the header allows you to do bulk sound assignment, which will be covered later.

#### Editing Playing Techniques 

Clicking on the name of the column opens a dialog that lets you edit that group of playing techniques:

![Axis](/axis-editor.png)

Here you can 
- change the name of the axis
- add or delete playing techniques from the axis
- move the axis left or right if that makes more sense to you
- add a new axis
- delete an axis. 

Fugalist provides a default set of axes to get started but, at minimum, you will probably want to
add additional playing techniques specific to the instrument to the **Techniques** axis.


### The Table Body

The body of the table is just a bunch or rows, one for each combination of the playing techniques. 
If you add or delete playing techniques, or rearrange the grouping, the rows of the table body will change 
to reflect that.

Here is one row:

![rows](/assignment-row.png)

The first five columns represent a particular combination of playing techniques, in this case a note marked
_non vibrato_ and _marcato_ in Dorico. (Remember that _Normal_ means the absence of any explicitly specified
playing technique.) The last column is a drop-down where you can pick any of the VST sounds or Composite sounds
that you've defined earlier. In this case, the VST contains a _marcato non-vibrato_ patch, so I used that.
The result will be that Dorico will play a note labeled with _non vibrato_ and _marcato_ using the **start** and
**stop** MIDI events specified for the _marcato non-vibrato_ sound.

One way (tedious, but possible) to create an expression map would be to go through every row of the table,
examine the playing techniques, select a VST or Composite sound, and assign it.
But frequently we can do better than that.

### Playing Technique Filters

The column header of the **Length** axis looks like this:

![axis-header](/axis-header.png)

We saw earlier that clicking on the top button opens the axis-editor dialog. Clicking on a playing technique such as
_staccato_ toggles the visibility of table rows containing that technique. 
I.e., if you toggle _Staccato_ off, all the rows containing _Staccato_ will be hidden. 
If you toggle it on again, they become visible.

You can toggle each playing technique individually. For example, if you toggle off everything except _Tenuto_
in the **Length** axis and toogle off everything except _Legato_ in the **Legato** axis, only rows that contain both
_Tenuto_ and _Legato_ will remain visible. 

(If you want to pick just one playing technique from an axis, you can double click it. It will be toggled on, and all
the others in that axis will be toggled off. The reset button toggles all the playing techniques _on_.)

Adjusting the playing technique filters is a convenient way to narrow in on a particular set of rows. 
For example, suppose your sample library has a "harsh" staccato patch. You might want to use that 
for at least some of the combinations that contain _Staccato_ or _Staccatissimo_ as well as _Marcato_.
Instead of scrolling around looking applicable rows, with a few
clicks you can focus in on exactly rows that have those playing techniques and then decide what to do.

### Bulk Assignment

Frequently, it's possible to manipulate playing technique filters so that all (or at least most of) the visible rows ought
get the same sound. 
For example, suppose that you add _Pizzicato_ to the **Techniques** axis. 
No matter what else is going on, if the note is marked _Pizzicato_ in Dorico, you probably want it played with your 
pizzicato patch.
Bulk sound assignment lets you do that.

The rightmost header in the assignment tab looks like this:

![Bulk](/bulk-assignment.png)

The top dropdown lets you pick any VST or Composite sound that you have defined.
The Apply button assigns that sound to all the visible rows in the table.
(If any visible rows are already assigned, it overwrites those assignments.)

The _Defined_ and _Undefined_ buttons are also filters. 
If you toggle _Defined_ to _off_, any table rows that have a sound already assigned to them are hidden.
This can be used to avoid overwriting existing assignments. 

If you assign the blank sound to a combination, the combination will not be written to the expression map. 
For example, if you are worried about expression-map size (I'm not) then you could reduce the size by un-defining
combinations that you don't ever intend to use.
