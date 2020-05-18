# Pure Data Reference

This is my personnal Pure Data reference following Dr. Rafael Hernandez' [tutorial](https://www.youtube.com/playlist?list=PL12DC9A161D8DC5DC) available on Youtube.

## 01 - Intro : Hello World

*See : 01_HelloWorld.pd*


Patching is done in a window called the **patcher** or **canvas**. It can be **locked** or **locked**. To be edited, it must be in the *unlocked* state. Toggle between *locked* and *unlocked* state using `CTRL + E`.

We can put different objects on the canvas : `object`, `object`, `number`, `symbol` and `comment`.  
These can be input using `CTRL` and respectively `1`, `2`, `3`, `4`, `5`.  
Objects can have receive and send values :
  - values are received through rectangles at the top called **inlets**
  - values are sent through rectangles at the bottom called **outlets**

*Inlets* and *outlets* from different objects must be **linked** in order for values to be transmitted between objects.

*Messages* objects can hold **string**, **int** and **float** values.
Clicking a message when the patcher is *locked* will send the message through its *links*.

To print something to the console, use the **print** object.  
Objects can have a list of **arguments** : these are specified after the object name, **separated by white spaces**.  
The print object has an optional name argument : it gives a name to its output in the console.

The **bang** object is created by creating an object with the name `bng`.
Bangs are used to **trigger events**, propagate values. **Clicking a bang while the patcher is locked will trigger it**.
A bang can also be created by creating a message containing the *string* "bang".

The console output can be cleared using `CTRL + MAJ + L`




## 02 - Getting help

To get some *help* with how an object works, create this object on the patcher, *right-click* it and click `Help`. This will open a new patch explaining how the object works, what are its *parameters*, *inlets* and *outlets*.

The leftmost inlet of an object is called the *hot inlet*.


## 03 - Basic math and bang order

When you need to hard store a value (e.g. *strings* or *integer*), use a *message* object.

In order to perform an addition, you must create an *object* with name `+`.  
It has two *inlets* (the *hot inlet* on the left), and one *outlet* to through which the result is yielded.  
Numeric results must be stored in `number` *objects*, they cannot be stored in `message` *objects*.  
A `number` object can store a numeric value, and propagate it through its *outlet*. **It cannot be used to declare new values**.

**A *bang* is propagated through its *outlet* in the order in which the *links* were created**.  
The *hot inlet* of an object (the leftmost *inlet*) will always *trigger* this object (i.e. execute the corresponding function and propagate the results) when it receives a *bang* or another kind of value. This means that, if a *bang* propagates multiple values to an object, and propagates a value to the *hot inlet* of this object before other values (because of the order in which the links were created), **the object will be triggered before having received all the values**. This is an important behavior to keep in mind.

In order to explicitly set the order in which the bangs will be sent, use the **trigger** object : an object with name `t`. Upon receiving a bang, this object will send out values or bangs in order from right to left. This can be used to **ensure that values are propagated in the right order**.

Once *cold inlets* receive a value, they store this value and use it every time the corresponding object is triggered, until they receive a new value.

