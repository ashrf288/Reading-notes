# Matplotlib


Python package for 2D-graphics



**IPython** is an enhanced interactive Python shell that has lots of interesting features including named inputs and outputs, access to shell commands, it allows interactive matplotlib sessions that have Matlab/Mathematica-like functionality.


**pyplot** majority of plotting commands in pyplot have Matlab(TM) analogs with similar arguments. Important commands are explained with interactive examples.


## Simple plot

## Changing colors and line widths 

`linewidth=2.5`

`linestyle="-"`

`color="blue"`

![](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/exercice_3.png)


## Setting limits

```
plt.xlim(X.min()*1.1, X.max()*1.1)
plt.ylim(C.min()*1.1, C.max()*1.1)

```

![](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/exercice_4.png)


## Setting ticks
(how the interesting values )

```
plt.xticks( [-np.pi, -np.pi/2, 0, np.pi/2, np.pi])
plt.yticks([-1, 0, +1])
```

![](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/exercice_6.png)


## Figures, Subplots, Axes and Ticks

We can have more control over the display using figure, subplot, and axes explicitly. 

A figure in matplotlib means the whole window in the user interface. Within this figure there can be subplots. While subplot positions the plots in a regular grid, axes allows free placement within the figure. Both can be useful depending on your intention. We've already worked with figures and subplots without explicitly calling them. 


## Figures

A figure is the windows in the GUI that has "Figure #" as title.

Figures are numbered starting from 1 as opposed to the normal Python way starting from 0

The defaults can be specified in the resource file and will be used most of the time. Only the number of the figure is frequently changed.

## Subplots

With subplot you can arrange plots in a regular grid. You need to specify the number of rows and columns and the number of the plot. Note that the gridspec command is a more powerful alternative.

![](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/subplot-horizontal.png)


## Axes
Axes are very similar to subplots but allow placement of plots at any location in the figure. So if we want to put a smaller plot inside a bigger one we do so with axes.

## Ticks

 Matplotlib provides a totally configurable system for ticks. There are tick **locators** to specify where ticks should appear and tick formatters to give ticks the appearance you want. Major and minor ticks can be located and formatted independently from each other





## Animation

animation in matplotlib was not an easy task and was done mainly through clever hacks. However, things have started to change since version 1.1 and the introduction of tools for creating animation very intuitively, with the possibility to save them in all kind of formats.


 most easy way to make an animation in matplotlib is to declare a FuncAnimation object that specifies to matplotlib what is the figure to update, what is the update function and what is the delay between frames.


## Drip drop

A very simple rain effect can be obtained by having small growing rings randomly positioned over a figure. Of course, they won't grow forever since the wave is supposed to damp with time.

![](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/rain.gif)


## Other Types of Plots

![](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/plot.png)

![](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/scatter.png)

![](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/bar.png)
