# Matplotlib tutorial
matplotlib is probably the single most used Python package for 2D-graphics.
It provides both a very quick way to visualize data from Python and publication-quality figures in many formats. 

## IPython
IPython is an enhanced interactive Python shell that has lots of interesting features including named inputs and outputs, access to shell commands, 
improved debugging and much more. It allows interactive matplotlib sessions that have Matlab/Mathematica-like functionality.

## pyplot
pyplot provides a convenient interface to the matplotlib object-oriented plotting library. It is modeled closely after Matlab(TM).
Therefore, the majority of plotting commands in pyplot have Matlab(TM) analogs with similar arguments.
Important commands are explained with interactive examples.


### Simple plot
In this section, we want to draw the cosine and sine functions on the same plot. Starting from the default settings, we'll enrich the figure step by step to make it nicer.

The first step is to get the data for the sine and cosine functions:

import numpy as np

X = np.linspace(-np.pi, np.pi, 256, endpoint=True)
C, S = np.cos(X), np.sin(X)
X is now a NumPy array with 256 values ranging from -π to +π (included). C is the cosine (256 values) and S is the sine (256 values).

To run the example, you can download each of the examples and run it using:

$ python exercice_1.py
You can get source for each step by clicking on the corresponding figure.




### Figures, Subplots, Axes and Ticks
So far we have used implicit figure and axes creation. This is handy for fast plots.
We can have more control over the display using figure, subplot, and axes explicitly. 
A figure in matplotlib means the whole window in the user interface. Within this figure there can be subplots. 
While subplot positions the plots in a regular grid, axes allows free placement within the figure. 
Both can be useful depending on your intention. We've already worked with figures and subplots without explicitly calling them. 
When we call plot, matplotlib calls gca() to get the current axes and gca in turn calls gcf() to get the current figure.
If there is none it calls figure() to make one, strictly speaking, to make a subplot(111). Let's look at the details.

Figures
A figure is the windows in the GUI that has "Figure #" as title. Figures are numbered starting from 1 as opposed to the normal Python way starting from 0. 
This is clearly MATLAB-style. There are several parameters that determine what the figure looks like:

Argument	Default	Description
num	1	number of figure
figsize	figure.figsize	figure size in in inches (width, height)
dpi	figure.dpi	resolution in dots per inch
facecolor	figure.facecolor	color of the drawing background
edgecolor	figure.edgecolor	color of edge around the drawing background
frameon	True	draw figure frame or not
The defaults can be specified in the resource file and will be used most of the time. Only the number of the figure is frequently changed.

When you work with the GUI you can close a figure by clicking on the x in the upper right corner. You can also close a figure programmatically by calling close. Depending on the argument it closes (1) the current figure (no argument), (2) a specific figure (figure number or figure instance as argument), or (3) all figures (all as argument).

As with other objects, you can set figure properties with the set_something methods.


Subplots
With subplot you can arrange plots in a regular grid. You need to specify the number of rows and columns and the number of the plot. 
Note that the gridspec command is a more powerful alternative.

Axes
Axes are very similar to subplots but allow placement of plots at any location in the figure. 
So if we want to put a smaller plot inside a bigger one we do so with axes.



Ticks
Well formatted ticks are an important part of publishing-ready figures. Matplotlib provides a totally configurable system for ticks.
There are tick locators to specify where ticks should appear and tick formatters to give ticks the appearance you want.
Major and minor ticks can be located and formatted independently from each other. By default minor ticks are not shown, i.e.
there is only an empty list for them because it is as NullLocator (see below).



Animation
For quite a long time, animation in matplotlib was not an easy task and was done mainly through clever hacks. However, 
things have started to change since version 1.1 and the introduction of tools for creating animation very intuitively, 
with the possibility to save them in all kind of formats (but don't expect to be able to run very complex animations at 60 fps though).

Documentation

See Animation
The most easy way to make an animation in matplotlib is to declare a FuncAnimation object that specifies to matplotlib what is the figure to update,
what is the update function and what is the delay between frames.

Drip drop
A very simple rain effect can be obtained by having small growing rings randomly positioned over a figure. Of course,
they won't grow forever since the wave is supposed to damp with time. To simulate that, we can use a more and more transparent color as the ring is growing,
up to the point where it is no more visible. At this point, we remove the ring and create a new one.

First step is to create a blank figure:

# New figure with white background
fig = plt.figure(figsize=(6,6), facecolor='white')

# New axis over the whole figure, no frame and a 1:1 aspect ratio
ax = fig.add_axes([0,0,1,1], frameon=False, aspect=1)

