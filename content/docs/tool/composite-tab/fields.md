---
weight: 10

---
# Fields

## Name

Give your composite sound a name.

## Condition

![Example](/composite-tab.png)

The condition determines which branch of the composite sound to use for a particular note. In the example above,
the first branch is used if the note length (as computed by Dorico) is less than **short**.
The second branch is used otherwise. That means that short notes will use your _staccato_ patch, and longer notes
use the _sustain_ patch.

The syntax for conditions is described in [Condition Syntax](/docs/tool/composite-tab/condition-syntax).

## Length

Enter a percentage if you want to adjust the note length.

{{< hint warning >}}
Remember that Dorico already modifies notated note lengths if certain playing techniques are active.
{{< /hint >}}

## Transpose

Enter a number (positive or negative) to transpose up or down by octaves.

## VST Sound

Select the VST sound to use for this branch. In the example above, short notes are played with the **staccato**
sound and longer notes played with the **sustain** sound.
Both of those are defined in the [VST sounds tab](/docs/tool/vst-tab).
