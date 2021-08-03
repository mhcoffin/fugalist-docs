---
weight: 3
---

# Action Buttons

## Download

This button downloads the latest version of the generated Dorico expression map to your local machine.
If you've made changes since the last download, it regenerates the map. If not, you get the same one as last time.

## Copy URL to clipboard

This button copies the URL of the latest version of the generated Dorico expression map. If you've made changes since
the last download, it regenerates the map. The URL remains the same for any single version of the expression map. The
URL changes when the version changes.

{{< hint warning >}}
The URL is difficult to guess, but it's **not** private. If you give the URL to a friend, they can
download your expression map. They can also pass the URL on to others, who will also be able to download it.
{{< /hint >}}

## Share

This button shares current state of your expression map and then increments the version.
The shared expression map will show up in the Fugalist search page, so anyone can find it and download it.

To share, you must have filled in a name, description, vendor, and instruments.

Even after you share, the previous shared version is still there, with the old URL.
{{< hint danger >}}
Bug: currently, Fugalist doesn't provide a direct way to get the URL of old versions of a shared expression map.
{{< /hint >}}

## Un-share

If you have shared a version and suddenly realize that you've made a horrible mistake that you don't want anyone to see,
you can un-share.
This doesn't actually delete anything, but it fixes things so that people browsing for maps won't see your expression
map until you share again (with a new version and URL).
