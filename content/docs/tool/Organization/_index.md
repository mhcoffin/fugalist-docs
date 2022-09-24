---
weight: 1
---

# Organization

The builder has six tabs to deal with different aspects of building an expression map.
When you create a new project, it starts you off in the Overview tab.

- The **Overview tab** is for metadata: expression-map name, instrument,
  VST library vendor, audio demos, etc. This is also the place to download your expression map for testing, or
  to share your expression map when you're happy with it.

- The **options** tab is for overriding playback options. If you want to change the playback duration of notes, change
  the way Dorico emphasizes the first beat of a bar, etc., this is the place to go. All entries on this tab apply
  to the entire expression map.

- The **VST Sounds** tab is where you specify the VST patches you want to use from your sample library.
  For each patch you want to use, you provide a name of your choosing, the on- and off-events,
  and the volume dynamic.

- The *Add-Ons*  tab is for adding add-on switches. For example, if your VST always uses CC1 to control vibrato, you can
  specify that here and not worry about vibrato ever again. In many cases, however, your VST isn't this well behaved,
  in which case you can skip this tab entirely. 

- The **Composite sounds tab** deals with note-length conditions, length factors, and transpositions.
  For many sample libraries, you can skip this tab entirely.

- The **Assignment Tab** is a fancy version of the table described in the
  [previous](/docs/introduction/example/#tiny-example) example.
  Using this tab, you can specify which techniques you
  want to support and how to group them.
  Then, for each combination of playing techniques,
  you can assign a sound, from either the VST Sounds tab or the Composite sounds tab.

  You can make sound assignments one row at a time, or you can select many rows at once (using technique filters)
  and assign a sound to all those rows.

The next sections go into more detail on each tab. 
