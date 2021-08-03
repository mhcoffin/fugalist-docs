---
weight: 50
title: So What's the Problem?
---
# What's the problem?

This all seems pretty straightforward: figure out which playing techniques to support. Then create a table with
one row for each combination of playing techniques. Assign on events, off events, etc., for each row.

The problem is scale.
Suppose you want to support
1. five note articulations (normal, staccato, staccatissimo, tenuto, and staccato-tenuto),
2. normal and legato note transitions
3. normal and marcato attack, and
4. normal and non- vibrato
5. normal, pizzicato, sul tasto, and sul pont.

That's 15 playing techniques, which means

    2^15 = 32768

table entries if you allow _any_ combination.

Luckily, the vast majority of combinations don't make any sense.
A note can't be marked both legato and non-legato at the
same time, nor can it be marked both staccato and staccatissimo.
So we can do much better by noticing that it only makes
sense to pick _one_ playing technique from each of the numbered sets.
That leaves

    5 * 2 * 2 * 2 * 3 = 120

sensible combinations. Still quite a few, but more manageable.

That's the problem the Fugalist expression-map builder attacks.
