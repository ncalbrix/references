# Reaper Personnal Reference

This file contains my personnal reference for using Reaper.
It adresses various features of the software.


## Tempo Mapping

*Keywords* : tempo mapping, tempo changes, rhythm signature

Place yourself at the start of your selection on your media item, and line it up with a tempo marker already present. With snapping turned on, split your media item at the tempo marker. Now place yourself at the end of your selection (multiple bars for a better result), having turned off snapping, and split your item at this place. Now **hold shift and double click** the created section, to create a **time selection**. Then, go to Insert -> Measure from time selection (new time signature). Enter the time signature and the number of bars, and click Ok. You can now glue back together the split item.
If you know your media item has been recorded to a click, you may now correct the calculated tempo to a round number.
If you want the whole project to have the newly calculated tempo, place yourself at the beginning of the timeline, and set the tempo value. Then, display the **Master Track** (View -> Master Track, or Ctrl + Alt + M), show the tempo enveloppe (click Envelopes, and click Visible for the Tempo Map), and delete the two points created when calculating the new tempo.



## Creating a marker

*Keywords* : marker, arrangement

Place yourself on the timeline at the point at which you want to create a marker. Right-click on the timeline and click on *Insert marker* or do Shift + M. A window appears where you can set the name and other characteristics of the marker. Click *OK* to create the marker. You can then move it around if you want by dragging it with the mouse, and change its name or color by right-clicking it and clicking on *Edit marker*, or simply by double-clicking it.



## Creating a region

*Keywords* : region, marker, arrangement

Create a **time selection** of where you want to create you region. Then, right-click on the timeline and click on *Create region from selection*, or use Shift + R. You can now edit the region by right-clicking on it and clicking on *Edit region*, or you can double-click on it while holding shift. You can then give it a name, a color, an ID, set its position and its length.

### Moving a region
When moving a region by clicking on it and dragging it across the timeline, you will actually **move every items it contains**. If you want to change the starting point of a region, you need to **edit it** and manually enter the starting point.

### Copying a region
You can copy a region by holding Ctrl and dragging the region at the point of the timeline where you want to copy it. Doing this will insert the content of the region of every tracks at this point of the timeline, and push the content that was there initially right after the region copy.