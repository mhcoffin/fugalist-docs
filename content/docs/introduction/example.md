---
weight: 30
title: Tiny Example
---

# Tiny Example

To be concrete, suppose we want to support the following playing techniques:

- Normal and tenuto lengths
- Normal and legato note connections
- Normal and pizzicato technique

Here's a complete table of sensible combinations, eight in all:

Length | Legato | Technique | on  | off  | vol | etc
------ | ------ | ----------| --------- | ---------- | -------------- | ---
Normal | Normal | Normal    |
Normal | Normal | Pizz      |
Normal | Legato | Normal    |
Normal | Legato | Pizz      |
Tenuto | Normal | Normal    |
Tenuto | Normal | Pizz      |
Tenuto | Legato | Normal    |
Tenuto | Legato | Pizz      |

What remains is to fill in the blanks: specify on events, off events, etc., for
each combination. The Fugalist expression-map tool is designed to do exactly that.
