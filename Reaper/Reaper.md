# Reaper Personnal Reference

This file contains my personnal reference for using Reaper.
It adresses various features of the software.


## Tempo Mapping

*Keywords* : tempo mapping, tempo changes, rhythm signature

Place yourself at the start of your selection on your media item, and line it up with a tempo marker already present. With snapping turned on, split your media item at the tempo marker. Now place yourself at the end of your selection (multiple bars for a better result), having turned off snapping, and split your item at this place. Now **hold shift and double click** the created section, to create a **time selection**. Then, go to Insert -> Measure from time selection (new time signature). Enter the time signature and the number of bars, and click Ok. You can now glue back together the split item.
If you know your media item has been recorded to a click, you may now correct the calculated tempo to a round number.
If you want the whole project to have the newly calculated tempo, place yourself at the beginning of the timeline, and set the tempo value. Then, display the **Master Track** (View -> Master Track, or Ctrl + Alt + M), show the tempo enveloppe (click Envelopes, and click Visible for the Tempo Map), and delete the two points created when calculating the new tempo.