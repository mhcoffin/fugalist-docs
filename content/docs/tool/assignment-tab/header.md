---
weight: 1
---

# The Assignment Table Header

The assignment-table header shows all the playing techniques that the expression map supports and how they are grouped.

Fugalist starts you off with a small selection of playing techniques applicable to almost any instrument:

![Header](/assignment-header.png)

Each column---**Length**, **Legato**, etc.---is called an _axis_. 
{{< hint info >}}
Fugalist will create a Dorico mutual-exclusion group for each axis (unless it contains only a single playing technique). 
{{< /hint >}}

You can use the [Axis Editor](/docs/tool/assignment-tab/axis-editor/#editing-playing-techniques) to add and delete
playing techniques or to add and delete entire axes.


- The first axis (**Length**) consists of the Dorico playing techniques that indicate note duration:
  _Normal_, _Staccato_, _Staccatissimo_, _Tenuto_,
  and _Staccato-tenuto_.
- The second axis (**Legato**) consists of _Normal_ and _Legato_.
- The third axis (**Vibrato**) consists of _Normal_ and _Non vibrato_.
- The fourth axis (**Attack**) consists of _Normal_ and _Marcato_.
- Finally, **Technique**, which initially contains only _Normal_. This is a good place to add special techniques that
  your instrument supports: _pizzicato_, _fluttertongue_, etc.

{{< hint info >}}
Every axis has a _Normal_ technique.
_Normal_ is not an actual Dorico playing technique.
_Normal_  means "no other playing technique from this group is active". 
For example, under **Length**, _Normal_ means "none of _staccato_, _staccatissimo_, _tenuto_, or _staccato-tenuto_
are active." 
{{< /hint >}}

The last column of the header allows you to do bulk sound assignment, 
which will be [covered later](/docs/tool/assignment-tab/bulk).
