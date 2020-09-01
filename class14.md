# Matplotlib

**Defintion**:
matplotlib is probably the single most used Python package for 2D-graphics. It provides both a very quick way to visualize data from Python and publication-quality figures in many formats.

* IPython and the pylab mode

IPython is an enhanced interactive Python shell that has lots of interesting features including named inputs and outputs, access to shell commands, improved debugging and much more.

* pyplot

pyplot provides a convenient interface to the matplotlib object-oriented plotting library. It is modeled closely after Matlab(TM).

* Simple plot

```
import numpy as np

X = np.linspace(-np.pi, np.pi, 256, endpoint=True)
C, S = np.cos(X), np.sin(X)
```

Where X is now a NumPy array with 256 values ranging from -π to +π (included). C is the cosine (256 values) and S is the sine (256 values).

### Changing colors and line widths

As a first step, we want to have the cosine in blue and the sine in red and a slightly thicker line for both of them. We'll also slightly alter the figure size to make it more horizontal.

```
plt.figure(figsize=(10,6), dpi=80)
plt.plot(X, C, color="blue", linewidth=2.5, linestyle="-")
plt.plot(X, S, color="red",  linewidth=2.5, linestyle="-")
```

### Adding a legend

```
plt.plot(X, C, color="blue", linewidth=2.5, linestyle="-", label="cosine")
plt.plot(X, S, color="red",  linewidth=2.5, linestyle="-", label="sine")

plt.legend(loc='upper left', frameon=False)
```


## Figures, Subplots, Axes and Ticks

1. Figures

    A figure is the windows in the GUI that has "Figure #" as title. Figures are numbered starting from 1 as opposed to the normal Python way starting from 0. This is clearly MATLAB-style. There are several parameters that determine what the figure looks like:
    ==============  ======================= ============================================
    Argument   |     Default        |         Description
    ------------|---------------------|------------------
    num         |    1                  |     number of figure
    figsize      |   figure.figsize        |  figure size in in inches (width, height)
    dpi          |   figure.dpi         |     resolution in dots per inch
    facecolor     |  figure.facecolor  |      color of the drawing background
    edgecolor     |  figure.edgecolor  |      color of edge around the drawing background
    frameon      |   True              |      draw figure frame or not
   

2. Subplots
    With subplot you can arrange plots in a regular grid. You need to specify the number of rows and columns and the number of the plot. Note that the gridspec command is a more powerful alternative.

3. Axes

    Axes are very similar to subplots but allow placement of plots at any location in the figure. So if we want to put a smaller plot inside a bigger one we do so with axes.

4. Ticks
    Well formatted ticks are an important part of publishing-ready figures. Matplotlib provides a totally configurable system for ticks. There are tick locators to specify where ticks should appear and tick formatters to give ticks the appearance you want. Major and minor ticks can be located and formatted independently from each other. By default minor ticks are not shown, i.e. there is only an empty list for them because it is as NullLocator


## Animation
    The most easy way to make an animation in matplotlib is to declare a FuncAnimation object that specifies to matplotlib what is the figure to update, what is the update function and what is the delay between frames.
    