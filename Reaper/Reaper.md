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



## Creating an enveloppe

*Keywords* : enveloppe, automation, parameter automation

In order to create an track enveloppe, or parameter automation, click on the *Track Enveloppes/Automation* button of the track (labeled with the word *trim*). This opens a window that lets you select the track parameters which you want to automate. These include the track primary parameter (volume, mute, panning), as well as the parameters of every effects or plugins that are on that track.Once you select a parameter, it appears in its own enveloppe lane, bellow the track, and a line represents the parameter's value through time.

### Creating points on the eveloppe lane
You can create points on the enveloppe lane by holding shift and clicking where you want to create the point (if *snapping* is enabled, it will affect the position where the point is created). You can then move a point, and it will change the value of the parameter.
If multiple points are created, you can move the section of the automation curve between two points by clicking on it and dragging it. The effect of doing this may vary according to the type of curve.

### Changing the type of curve
By default, the transition from one point to another will be linear. You can change the type of curve that will connect one point to the next by right-clicking on that point, and selecting the curve type in the sub-menu *Set point shape*. You can also change the default shape for every point of this enveloppe by right-clicking on the enveloppe, and selecting the shape in the sub-menu *Enveloppe defaults -> Default point shape*.

### Selecting multiple points
You can select multiple points of an enveloppe by holding Ctrl and clicking on each point you want to select.
You can also create a rectangle selection by holding the right click and moving the mouse.

### Drawing an enveloppe
You can draw your own enveloppe by holding Ctrl and the left click, and moving the mouse across the enveloppe lane. This will actually create a number of points, that can then be edited on by one.

### Moving and enveloppe from its enveloppe lane
You can make it so the enveloppe appears on the track rather than on its own lane (though it can become cluttered if you put multiple enveloppes there). In order to do so, click on the *Hide/Clear* menu right next to the enveloppe name, and click on *Move to media lane*. The enveloppe will then appear on the media.
If you want to move an enveloppe back to its own lane, right-click on it and click on *Show enveloppe in lane*.