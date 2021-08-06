---
weight: 5
title: Bulk Assignment
---

# Bulk Assignment

Frequently, after focusing in on some rows, you want to apply the same sound to all the visible rows.
To continue the example from the previous section, you might want to assign "harsh staccato" to 
all the rows that have _marcato_ in addition to either _staccato_ or _staccatissimo_.
Bulk sound assignment lets you do that.

The rightmost header in the assignment tab looks like this:

![Bulk](/bulk-assignment.png)

The top dropdown (initially blank) lets you pick any VST or Composite sound that you've defined.
The **Apply** button assigns that sound to all the **visible** rows in the table.
If any visible rows already have a sound assigned, **Apply** overwrites those assignments.

The _Defined_ and _Undefined_ buttons are additional filters: toggling _Defined_ off hides all the rows
that have a sound already assigned. Similarly, toggling _Undefined_ off hides rows where no sound has been assigned.
One use for these toggles is to avoid overwriting existing assignments.

If you assign the blank sound ("---") to a combination, that combination will not be written to the expression
map at all.
