---
weight: 1
---

# The Assignment Table Header

The assignment-table header shows all the playing techniques that the expression map supports and how they are grouped. 

![Header](/assignment-header.png)

Each column is called an _axis_.

- The first axis (**Length**) consists of the Dorico playing techniques that indicate note duration:
  _Normal_, _Staccato_, _Staccatissimo_, _Tenuto_,
  and _Staccato-tenuto_.
- The second axis (**Legato**) consists of _Normal_ and _Legato_.
- The third axis (**Vibrato**) consists of _Normal_ and _Non vibrato_.
- The fourth axis (**Attack**) consists of _Normal_ and _Marcato_.
- Finally, **Technique**, which contains only _Normal_ for now.

{{< hint info >}}
Every axis has a _Normal_ technique. 
_Normal_ is not an actual playing technique. 
_Normal_  means "no other playing technique from this group is active". 
For example, under **Length**, _Normal_ means "none of _staccato_, _staccatissimo_, _tenuto_, or _staccato-tenuto_
are active."
{{< /hint >}}

The last column of the header allows you to do bulk sound assignment, 
which will be [covered later](/docs/tool/assignment-tab/bulk).

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
add to the **Techniques** axis additional playing techniques specific to the instrument.
