# Reaper Personnal Reference

This file contains my personnal reference for using Reaper.
It adresses various features of the software.



## Misc tips

*Keywords* : time selection

### Extend a time selection from anywhere
Let's say you have an existing time selection on your project. You extend it from anywhere by holding Shift, and clicking and dragging on the time ruler (at the top of the track lanes) or on an empty space in a track.

### Move a time selection
In order to move a time selection, you need to hold Shift, click somewhere empty in the time selection (on a track with empty space, or on the time ruler), and drag the time selection where you want to place it.



## Project setup

*Keywords* : paths, options, default, media copy, media import

### Writing all media files into project media subdirectory
Open the project settings (Alt + Enter), an go to the *Media* tab. There, input a subdirectory name in the *Path to save media files* box, such as *media*. If you want all you projects to use the same settings by default, you can click on the *Save as default project settings* button at the bottom right of the peoject settings window.

### Copying all imported media files into project media subdirectory
It can be useful to copy all imported media files in the project media subdirectory (refer to the previous section), making the project self-contained if you need for instance to send it over to other persons, or move it to another location on the computer, or to another computer. Keep in mind though that it can be quite demanding in storage space on the hard drive if mant items are imported (e.g. samples).
In order to activate this option, go to *Options -> Preferences -> Media* and check the box *Copy imported media to project media directory*, then click *Apply*.



## Tempo Mapping

*Keywords* : tempo mapping, tempo changes, rhythm signature

Place yourself at the start of your selection on your media item, and line it up with a tempo marker already present. With snapping turned on, split your media item at the tempo marker. Now place yourself at the end of your selection (multiple bars for a better result), having turned off snapping, and split your item at this place. Now **hold shift and double click** the created section, to create a **time selection**. Then, go to *Insert -> Measure from time selection (new time signature)*. Enter the time signature and the number of bars, and click Ok. You can now glue back together the split item.
If you know your media item has been recorded to a click, you may now correct the calculated tempo to a round number.
If you want the whole project to have the newly calculated tempo, place yourself at the beginning of the timeline, and set the tempo value. Then, display the **Master Track** (*View -> Master Track*, or Ctrl + Alt + M), show the tempo envelope (click *Track Envelopes/Automation*, and click *Visible* for the Tempo Map), and delete the two points created when calculating the new tempo.



## Creating a marker

*Keywords* : marker, arrangement

Place yourself on the timeline at the point at which you want to create a marker. Right-click on the timeline and click on *Insert marker* or do Shift + M. A window appears where you can set the name and other characteristics of the marker. Click *OK* to create the marker. You can then move it around if you want by dragging it with the mouse, and change its name or color by right-clicking it and clicking on *Edit marker*, or simply by double-clicking it.



## Creating a region

*Keywords* : region, marker, arrangement

Create a **time selection** of where you want to create you region. Then, right-click on the timeline and click on *Create region from selection*, or use Shift + R. You can now edit the region by right-clicking on it and clicking on *Edit region*, or you can double-click on it while holding Shift. You can then give it a name, a color, an ID, set its position and its length.

### Moving a region
When moving a region by clicking on it and dragging it across the timeline, you will actually **move every items it contains**. If you want to change the starting point of a region, you need to **edit it** and manually enter the starting point.

### Copying a region
You can copy a region by holding Ctrl and dragging the region at the point of the timeline where you want to copy it. Doing this will insert the content of the region of every tracks at this point of the timeline, and push the content that was there initially right after the region copy.



## Creating an envelope

*Keywords* : envelope, automation, parameter automation

In order to create an track envelope, or parameter automation, click on the *Track Envelopes/Automation* button of the track (labeled with the word *trim*). This opens a window that lets you select the track parameters which you want to automate. These include the track primary parameter (volume, mute, panning), as well as the parameters of every effects or plugins that are on that track.Once you select a parameter, it appears in its own envelope lane, bellow the track, and a line represents the parameter's value through time.

### Creating points on the eveloppe lane
You can create points on the envelope lane by holding shift and clicking where you want to create the point (if *snapping* is enabled, it will affect the position where the point is created). You can then move a point, and it will change the value of the parameter.
If multiple points are created, you can move the section of the automation curve between two points by clicking on it and dragging it. The effect of doing this may vary according to the type of curve.

### Changing the type of curve
By default, the transition from one point to another will be linear. You can change the type of curve that will connect one point to the next by right-clicking on that point, and selecting the curve type in the sub-menu *Set point shape*. You can also change the default shape for every point of this envelope by right-clicking on the envelope, and selecting the shape in the sub-menu *Envelope defaults -> Default point shape*.

### Selecting multiple points
You can select multiple points of an envelope by holding Ctrl and clicking on each point you want to select.
You can also create a rectangle selection by holding the right click and moving the mouse.

### Drawing an envelope
You can draw your own envelope by holding Ctrl and the left click, and moving the mouse across the envelope lane. This will actually create a number of points, that can then be edited on by one.

### Moving and envelope from its envelope lane
You can make it so the envelope appears on the track rather than on its own lane (though it can become cluttered if you put multiple envelopes there). In order to do so, click on the *Hide/Clear* menu right next to the envelope name, and click on *Move to media lane*. The envelope will then appear on the media.
If you want to move an envelope back to its own lane, right-click on it and click on *Show envelope in lane*.



## Creating an automation item

*Keywords* : automation, envelope, automation item

In order to create an **automation item** for a parameter of a track, you must first open the envelope lane of this parameter. Then, hold Alt, and click and drag just under the envelope curve for the desired duration of the automation item. It the creates an automation item, and two points, at the beginning and at the end of the item

### Changing the curve shape between two points
You can change the curve shape between two points in an automation item (faster rise, or slower rise) by holding Alt, and clicking and dragging the curve between the two points.



## Changing the snap offset of an item

*Keywords* : snapping, grid, snap offset, reverse cymbal

When you want an item to snap to the grid at some other point than its beginning (typically when using a reverse cymbal sample, you want the end of the sample to snap to the grid), you need to change its snap offset. In order to do so, place your mouse on the snap offset marker (a white triangle at the bottom of the item, by default it should be in the lower left corner, and your cursor will change when your mouse hover over it), click on it and drag it where you want your item to snap to the grid. In order to move it freely, you can hold Shift while moving it.



## Fast import of samples and media files using the Media Explorer

*Keywords* : sample, media file, file explorer, media explorer

A good solution to quickly and easily import samples, sounds, songs, or any media file in your Reaper project is to use the Media Explorer. You can open it with the menu *View -> Media Explorer* or by using the shortcut Ctrl + Alt + X. You can dock it to the bottom or to one side of the Reaper window for more clarity.
The Media Explorer allows you to browse files on your file system, play them, and import them into the project. It also offers some (limited) editing capabilities : pitch, replay rate, time selection.

### Quickly import sample on new track
In order to import a sample on a new track using the Media Explorer, place the time cursor at the point in time of the project where you want to import the sample, then right-click on the sample in the Media Explorer, and click on *Insert on a new track*.