---
weight: 3
---

# Action Buttons

## Download

Clicking the download button first regenerates the expression map if changes have been made. 
Then it downloads the latest version of the generated Dorico expression map to your local machine.

## Copy URL to clipboard

This button copies the URL of the latest version of the generated Dorico expression map.
The URL remains the same for each version of the expression map. 
The URL changes when the version changes.

{{< hint warning >}}
The URL of an expression map is difficult to guess, but it's **not** private. 
If you give the URL to a friend, they can download your expression map. 
They can also pass the URL on to others, who will also be able to download it.
{{< /hint >}}

## Share

This button shares your expression map in its current state and then increments the version.
The shared expression map will show up in the Fugalist search page, so anyone can find it and download it.

To share, you must have filled in at least a name, description, vendor, and instruments.

Even after you share, the previous shared version is still there, with the old URL.
{{< hint danger >}}
Bug: currently, Fugalist doesn't provide a direct way to get the URL of old versions of a shared expression map.
{{< /hint >}}

## Un-share

If you have shared a version of your expression map and then suddenly realize that you've made a horrible mistake, you can un-share.
This doesn't actually delete anything, but it fixes things so that people browsing for maps won't see your expression
map until you share again.

{{< hint danger >}}
Bug: currently, if someone already has the URL for an un-shared expression map, they can still download it.  
{{< /hint >}}
