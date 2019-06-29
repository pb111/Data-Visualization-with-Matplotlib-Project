 # Data Visualization with Matplotlib

This project is all about **Matplotlib**, the basic data visualization tool of Python programming language. In this project, I have discussed Matplotlib, its object hierarchy, various plot types with Matplotlib and customization techniques associated with Matplotlib. 

===============================================================================

This project is divided into various sections based on contents which are listed below:- 

## Table of Contents

1.	Introduction
2.	Overview of Python Data Visualization Tools
3.	Introduction to Matplotlib
4.	Import Matplotlib
5.	Displaying Plots in Matplotlib
6.	Matplotlib Object Hierarchy
7.	Matplotlib interfaces
8.	Pyplot API
9.	Object-Oriented API
10.	Figure and Subplots
11.	First plot with Matplotlib
12.	Multiline Plots
13.	Parts of a Plot 
14.	Saving the Plot
15.	Line Plot
16.	Scatter Plot
17.	Histogram
18.	Bar Chart
19.	Horizontal Bar Chart
20.	Error Bar Chart
21.	Stacked Bar Chart
22.	Pie Chart
23.	Box Plot
24.	Area Chart
25.	Contour Plot
26.	Styles with Matplotlib Plots
27.	Adding a grid
28.	Handling axes
29.	Handling X and Y ticks
30.	Adding labels 
31.	Adding a title
32.	Adding a legend
33.	Control colours
34.	Control line styles 
35.	Summary
36. References

===============================================================================


## 1.	Introduction

When we want to convey some information to others, there are several ways to do so. The process of conveying the information with the help of plots and graphics is called **Data Visualization**. The plots and graphics take numerical data as input and display output in the form of charts, figures and tables. It helps to analyze and visualize the data clearly and make concrete decisions. It makes complex data more accessible and understandable. The goal of data visualization is to communicate information in a clear and efficient manner.


In this project, I shed some light on Matplotlib, which is the basic data visualization tool of Python programming language. Python has different data visualization tools available which are suitable for different purposes. First of all, I will list these data visualization tools and then I will discuss Matplotlib.


===============================================================================


## 2.	Overview of Python Data Visualization Tools


Python is the preferred language of choice for data scientists. Python have multiple options for data visualization. It has several tools which can help us to visualize the data more effectively. These Python data visualization tools are as follows:-


•	Matplotlib

•	Seaborn

•	pandas

•	Bokeh

•	Plotly

•	ggplot

•	pygal


In the following sections, I discuss Matplotlib as the data visualization tool. 


===============================================================================

## 3. Introduction to Matplotlib


**Matplotlib** is the basic plotting library of Python programming language. It is the most prominent tool among Python visualization packages. Matplotlib is highly efficient in performing wide range of tasks. It can produce publication quality figures in a variety of formats.  It can export visualizations to all of the common formats like PDF, SVG, JPG, PNG, BMP and GIF. It can create popular visualization types – line plot, scatter plot, histogram, bar chart, error charts, pie chart, box plot, and many more types of plot. Matplotlib also supports 3D plotting. Many Python libraries are built on top of Matplotlib. For example, pandas and Seaborn are built on Matplotlib. They allow to access Matplotlib’s methods with less code. 


The project **Matplotlib** was started by John Hunter in 2002. Matplotlib was originally started to visualize Electrocorticography (ECoG) data of epilepsy patients during post-doctoral research in Neurobiology. The open-source tool Matplotlib emerged as the most widely used plotting library for the Python programming language. It was used for data visualization during landing of the Phoenix spacecraft in 2008.

===============================================================================

## 4.	Import Matplotlib

Before, we need to actually start using Matplotlib, we need to import it. We can import Matplotlib as follows:-

`import matplotlib`


Most of the time, we have to work with **pyplot** interface of Matplotlib. So, I will import **pyplot** interface of Matplotlib as follows:-

`import matplotlib.pyplot`

To make things even simpler, we will use standard shorthand for Matplotlib imports as follows:-


`import matplotlib.pyplot as plt`


From now onwards, I will refer matplotlib.pyplot as plt.


===============================================================================

## 5.	 Displaying Plots in Matplotlib

Viewing the Matplotlib plot is context based. The best usage of Matplotlib differs depending on how we are using it. There are three applicable contexts for viewing the plots. The three applicable contexts are using plotting from a script, plotting from an IPython shell or plotting from a Jupyter notebook.



### Plotting from a script

If we are using Matplotlib from within a script, then the **plt.show()** command is of great use. It starts an event loop, looks for all currently active figure objects, and opens one or more interactive windows that display the figure or figures.
The **plt.show()** command should be used only once per Python session. It should be used only at the end of the script. Multiple **plt.show()** commands can lead to unpredictable results and should mostly be avoided.


### Plotting from an IPython shell

We can use Matplotlib interactively within an IPython shell. IPython works well with Matplotlib if we specify Matplotlib mode. To enable this mode, we can use the %matplotlib magic command after starting ipython. Any plt plot command will cause a figure window to open and further commands can be run to update the plot.


### Plotting from a Jupyter notebook

The Jupyter Notebook (formerly known as the IPython Notebook) is a data analysis and visualization tool that provides multiple tools under one roof.  It provides code execution, graphical plots, rich text and media display, mathematics formula and much more facilities into a single executable document.

Interactive plotting within a Jupyter Notebook can be done with the **%matplotlib** command. There are two possible options to work with graphics in Jupyter Notebook. These are as follows:-

•	%matplotlib notebook – This command will produce interactive plots embedded within the notebook.

•	%matplotlib inline – It will output static images of the plot embedded in the notebook.

After this command (it needs to be done only once per kernel per session), any cell within the notebook that creates a plot will embed a PNG image of the graphic.

===============================================================================

## 6.	 Matplotlib Object Hierarchy


There is an Object Hierarchy within Matplotlib. In Matplotlib, a plot is a hierarchy of nested Python objects. A**hierarchy** means 
that there is a tree-like structure of Matplotlib objects underlying each plot.


A **Figure** object is the outermost container for a Matplotlib plot. The **Figure** object contain multiple **Axes** objects. 
So, the **Figure** is the final graphic that may contain one or more **Axes**. 


The **Axes** represent an individual plot.


So, we can think of the **Figure** object as a box-like container containing one or more **Axes**. The **Axes** object contain smaller objects such as tick marks, lines, legends, title and text-boxes.


===============================================================================

## 7.	Matplotlib API Overview

 Matplotlib has two APIs to work with. 
 
A **MATLAB-style state-based interface** and a more powerful **Object-Oriented (OO) interface**. 

The former MATLAB-style state-based interface is called **pyplot interface** and the latter is called **Object-Oriented** interface.

There is a third interface also called **pylab** interface. It merges pyplot (for plotting) and NumPy (for mathematical functions) together in an environment closer to MATLAB. This is considered bad practice nowadays. So, the use of **pylab** is strongly discouraged and hence, I will not discuss it any further.

===============================================================================

## 8.	Pyplot API 

**Matplotlib.pyplot** provides a MATLAB-style, procedural, state-machine interface to the underlying object-oriented library in Matplotlib. **Pyplot** is a collection of command style functions that make Matplotlib work like MATLAB. Each pyplot function makes some change to a figure: e.g., creates a figure, creates a plotting area in a figure etc. 

**Matplotlib.pyplot** is stateful because the underlying engine keeps track of the current figure and plotting area information and plotting functions change that information. To make it clearer, we did not use any object references during our plotting we just issued a pyplot command, and the changes appeared in the figure.

We can get a reference to the current figure and axes using the following commands-

`plt.gcf ( )`   # get current figure

`plt.gca ( )`   # get current axes  
 
**Matplotlib.pyplot** is a collection of commands and functions that make Matplotlib behave like MATLAB (for plotting). The MATLAB-style tools are contained in the pyplot (plt) interface. 


This is really helpful for interactive plotting, because we can issue a command and see the result immediately. But, it is not suitable for more complicated cases. For these cases, we have another interface called **Object-Oriented** interface, described later.

===============================================================================

## 9.	Object-Oriented API

The **Object-Oriented API** is available for more complex plotting situations. It allows us to exercise more control over the figure. In Pyplot API, we depend on some notion of an "active" figure or axes. But, in the **Object-Oriented API** the plotting functions are methods of explicit Figure and Axes objects.

**Figure** is the top level container for all the plot elements. We can think of the **Figure** object as a box-like container containing one or more **Axes**. 

The **Axes** represent an individual plot. The **Axes** object contain smaller objects such as axis, tick marks, lines, legends, title and text-boxes.


### Objects and Reference

The main idea with the Object Oriented API is to have objects that one can apply functions and actions on. The real advantage of this approach becomes apparent when more than one figure is created or when a figure contains more than one subplot.


We create a reference to the figure instance in the fig variable. Then, we ceate a new axis instance axes using the add_axes method in the Figure class instance fig.

I start by creating a figure and an axes. A figure and axes can be created as follows:


`fig = plt.figure()`

`ax = plt.axes()`


In Matplotlib, the **figure** (an instance of the class plt.Figure) is a single container that contains all the objects representing axes, graphics, text and labels. The **axes** (an instance of the class plt.Axes) is a bounding box with ticks and labels. It will contain the plot elements that make up the visualization. I have used the variable name fig to refer to a figure instance, and ax to refer to an axes instance or group of axes instances.


### Figure and Axes

I start by creating a figure and an axes. A figure and axes can be created as follows:

`fig = plt.figure()`

`ax = plt.axes()`

In Matplotlib, the **figure** (an instance of the class plt.Figure) is a single container that contains all the objects representing axes, graphics, text and labels. The **axes** (an instance of the class plt.Axes) is a bounding box with ticks and labels. It will contain the plot elements that make up the visualization. I have used the variable name fig to refer to a figure instance, and ax to refer to an axes instance or group of axes instances.

===============================================================================

## 10.	Figures and Subplots

Plots in Matplotlib reside within a Figure object. As described earlier, we can create a new figure with plt.figure() as follows:-

`fig = plt.figure()`

Now, I create one or more subplots using fig.add_subplot() as follows:-

`ax1 = fig.add_subplot(2, 2, 1)`

The above command means that there are four plots in total (2 * 2 = 4). I select the first of four subplots (numbered from 1).


I create the next three subplots using the fig.add_subplot() commands as follows:-

`ax2 = fig.add_subplot(2, 2, 2)`

`ax3 = fig.add_subplot(2, 2, 3)`

`ax4 = fig.add_subplot(2, 2, 4)`


The above command result in creation of subplots as follows:-


![Diagrammatic representation of subplots](https://github.com/pb111/Data-Visualization-with-Matplotlib-Project/blob/master/Images/Subplots.png)


### Concise representation of Subplots

There is a concise form by which we can represent Subplots. Matplotlib includes a convenience method plt.subplots() that creates a new figure and returns the subplot objects. We can create subplots as follows:-

`fig, axes = plt.subplots()`

The above command creates a figure and one subplot. It is short and concise representation of the following commands:-

`fig = plt.figure()`

`ax1 = fig.add_subplot(1, 1, 1)`

We get a reference to both figure and axis in a single step.


### More than one Subplot

We can use


`fig, axes = plt.subplots(nrows = 2, ncols = 2)`

to create four Subplots with grid(2, 2) in one figure object.


===============================================================================

## 11.	First plot with Matplotlib

Now, I will start producing plots. Here is the first example:-

`plt.plot([1, 3, 2, 4] )`

`plt.show( )`

This code line is the actual plotting command. Only a list of values has been plotted that represent the vertical coordinates of the points to be plotted. Matplotlib will use an implicit horizontal values list, from 0 (the first value) to N-1 (where N is the number of items in the list).

Also, we can explicitly specify both the lists as follows:- 

 `x = np.arange(0.0, 6.0,  0.01)` 

 `plt.plot(x, [xi**2 for xi in x])` 

`plt.show()`

===============================================================================

## 12.	Multiline Plots

Multiline Plots mean plotting more than one plot on the same figure. We can plot more than one plot on the same figure.  It can be achieved by plotting all the lines before calling show() as follows:-

`x4 = range(1, 5)`

`plt.plot(x4, [xi*1.5 for xi in x4])`

`plt.plot(x4, [xi*3 for xi in x4])`

`plt.plot(x4, [xi/3.0 for xi in x4])`

`plt.show()`

===============================================================================

## 13.	Parts of a Plot

There are different parts of a plot. These are title, legend, grid, axis and labels etc. These are denoted in the following figure:-


![Parts of a Plot](https://github.com/pb111/Data-Visualization-with-Matplotlib-Project/blob/master/Images/Parts%20of%20a%20plot.png)


===============================================================================


## 14.	Saving the Plot

We can save the figures in a wide variety of formats. We can save them using the **savefig()** command as follows:-

`fig.savefig(‘fig1.png’)`

We can explore the contents of the file using the IPython **Image** object.

`from IPython.display import Image`

`Image(‘fig1.png’)`

In **savefig()** command, the file format is inferred from the extension of the given filename. Depending on our backend, many different file formats are available. The list of supported file types can be found by using the get_supported_filetypes() method of the figure canvas object as follows:-

`fig.canvas.get_supported_filetypes()` 

===============================================================================

## 15.	Line Plot

We can use the following commands to draw the simple sinusoid line plot:-


`x5 = np.linspace(0, 10, 1000)`

`ax.plot(x5, np.sin(x5));` 


Alternatively, we can use the Pyplot interface and let the figure and axes be created for us in the background.

`plt.plot(x5, np.sin(x5));`

Similarly, if we want to create a single figure with multiple lines, we can call the plot function multiple times.

`plt.plot(x6, np.sin(x6), ‘b-‘)`

`plt.plot(x6, np.cos(x6), ‘r-‘)`

===============================================================================

## 16.	Scatter Plot

Another commonly used plot type is the scatter plot. Here the points are represented individually with a dot or a circle.

•	Scatter Plot with plt.plot()

We have used plt.plot/ax.plot to produce line plots. We can use the same functions to produce the scatter plots as follows:-

`x7 = np.linspace(0, 10, 1000)`

`y7 = np.sin(x7)`

`plt.plot(x7, y7, ‘o’, color = ‘black’)`

We can customize the plot by combining the character codes together with line and color codes to plot points along with a line connecting them as follows:-

`plt.plot(x7, y7, ‘-ok’)`


•	Scatter Plot with plt.scatter()


An alternative approach of creating scatter plot is to use plt.scatter() function. It is more powerful method of creating scatter plots than to use the plt.plot() function. We can use plt.scatter() function as follows:-

`plt.scatter(x7, y7, ‘-o’)`

`plt.show()`

The primary difference of plt.scatter() function from plt.plot() is that it can be used to create scatter plots where the properties of each individual point (size, face color, edge color, etc.) can be individually controlled or mapped to the data.


•	plt.plot() Vs plt.scatter() functions

For smaller datasets, it does not matter whether we use plt.plot() or plt.scatter() functions to create scatter-plots.
But for larger datasets, plt.plot() function is more efficient than plt.scatter() function. In plt.plot() function, the points are clones of each other. So the work of determining the appearance of the points is done only once for the entire set of data. In plt.scatter() function, the renderer must do the extra work of constructing each point individually.


So, for large datasets, the difference between plt.plot() and plt.scatter() functions can lead to vastly different performance.  Hence, plt.plot() function should be preferred over plt.scatter() function for large datasets.

===============================================================================

## 17.	Histogram

Histogram charts are a graphical display of frequencies. They are represented as bars. They show what portion of the dataset falls into each category, usually specified as non-overlapping intervals. These categories are called **bins**.

The **hist()** function can be used to plot a simple histogram as follows:-


`data = np.random.randn(1000)`

`plt.hist(data)`


The plt.hist() function has many parameters to tune both the calculation and the plot display. We can see these parameters in action as follows:-
 

`plt.hist(data, bins=30, density=True, alpha=0.5, histtype='stepfilled', color='steelblue')`

`plt.show();`



### Compare Histograms of several distributions


We can use the combination of histtype=’stepfilled’ along with transparency level alpha to compare histograms of several distributions.


`x1 = np.random.normal(0, 1, 1000)`

`x2 = np.random.normal(-1, 1, 1000)`

`x3 = np.random.normal(1, 4, 1000)`

`kwargs = dict(histtype=’stepfilled’, alpha = 0.2, density = True, bins = 30)`

`plt.hist(x1, **kwargs)`

`plt.hist(x2, **kwargs)`

`plt.hist(x3, **kwargs)`

`plt.show()`


## Two-Dimensional Histograms


Just as we create histograms in one dimension, we can also create histograms in two-dimensions by dividing points among two-dimensional bins. We can use Matplotlib’s **hist2d()** function to plot a two-dimensional histogram as follows:-


`mean = [0, 0]`

`cov = [[1, 1], [1, 2]]`

`x8, y8 = np.random.multivariate_normal(mean, cov, 10000).T`

`plt.hist2d(x8, y8, bins = 30, cmap = 'Blues')`

`cb = plt.colorbar()`

`cb.set_label('counts in bin')`

===============================================================================

## 18.	Bar Chart

Bar charts display rectangular bars either in vertical or horizontal form. Their length is proportional to the values they represent. They are used to compare two or more values.

We can plot a bar chart using **bar( )** function. We can plot a bar chart as follows:-

`data2 = [5. , 25. , 50. , 20.]`

`plt.bar(range(len(data2)), data2)`

`plt.show()` 


### The thickness of the Bar Chart

By default, a bar will have a thickness of 0.8 units. If we draw a bar of unit length, we have a gap of 0.2 between them. We can change the thickness of the bar chart by setting width parameter to 1.

`plt.bar(range(len(data2)), data2, width = 1)`

`plt.show()` 

===============================================================================

## 19.	Horizontal Bar Chart

We can produce Horizontal Bar Chart using the **barh()** function. It is the strict equivalent of bar() function.

`data2 = [5. , 25. , 50. , 20.]`

`plt.barh(range(len(data2)), data2)`

`plt.show()` 

===============================================================================

## 20.	Error Bar Chart

In experimental design, the measurements lack perfect precision. So, we have to repeat the measurements. It results in  obtaining 
a set of values. The representation of the distribution of data values is done by plotting a single data point (known as mean value 
of dataset) and an error bar to represent the overall distribution of data.


We can use Matplotlib's **errorbar()** function to represent the distribution of data values.


### Asymmetrical Error Bars

The error bars described in the previous section, are called **symmetrical error bars**. Their negative error is equal in value to 
the positive error. So error bar is symmetrical to the point where it is drawn. 


There is another type of error bar, which is **asymmetrical error bar**. To draw **asymmetrical error bars**, we have to pass two lists(or a 2D array) of values to yerr and/or xerr - the first list is for negative errors while the second list is for positive 
errors.

===============================================================================

## 21.	Stacked Bar Chart


We can draw stacked bar chart by using a special parameter called **bottom** from the plt.bar() function.


===============================================================================

## 22. Pie Chart

Pie charts are circular representations, divided into sectors. The sectors are also called **wedges**. The arc length of each sector 
is proportional to the quantity we are describing. It is an effective way to represent information when we are interested mainly in comparing the wedge against the whole pie, instead of wedges against each other.

Matplotlib provides the **pie()** function to plot pie charts from an array X. Wedges are created proportionally, so that each value x of array X generates a wedge proportional to x/sum(X).


## Exploded Pie Chart

We can plot an exploded Pie chart with the addition of keyword argument **explode**. It is an array of the same length as that of X. Each of its values specify the radius fraction with which to offset the wedge from the center of the pie.

===============================================================================

## 23. Boxplot

Boxplot allows us to compare distributions of values by showing the median, quartiles, maximum and minimum of a set of values. We can plot a boxplot with the **boxplot()** function.

===============================================================================

## 24. Area Chart

An **Area Chart** is very similar to a **Line Chart**. The area between the x-axis and the line is filled in with color or shading. 
It represents the evolution of a numerical variable following another numerical variable.

===============================================================================

## 25. Contour Plot

**Contour plots** are useful to display three-dimensional data in two dimensions using contours or color-coded regions. 
**Contour lines** are also known as **level lines** or **isolines**. **Contour lines** for a function of two variables are curves 
where the function has constant values. They have specific names beginning with iso- according to the nature of the variables being mapped.


There are lot of applications of **Contour lines** in several fields such as meteorology(for temperature, pressure, rain, wind speed), geography, magnetism, engineering, social sciences and so on.


The density of the lines indicates the **slope** of the function. The **gradient** of the function is always perpendicular to the contour lines. When the lines are close together, the length of the gradient is large and the variation is steep.

A **Contour plot** can be created with the **plt.contour()** function.

===============================================================================

## 26. Styles with Matplotlib Plots

The Matplotlib version 1.4 which was released in August 2014 added a very convenient `style` module. It includes a number of  new default stylesheets, as well as the ability to create and package own styles.

We can view the list of all available styles by the following command.

`print(plt.style.availabe)`

We can set the Styles for Matplotlib plots as follows:-

plt.style.use('seaborn-bright')

I have set the seaborn-bright style for plots. So, the plot uses the seaborn-bright Matplotlib style for plots.

===============================================================================

## 27. Adding a grid

In some cases, the background of a plot was completely blank. We can get more information, if there is a reference system in the plot. The reference system would improve the comprehension of the plot. An example of the reference system is adding a **grid**.


We can add a grid to the plot by calling the **grid()** function. It takes one parameter, a Boolean value, to enable(if True) or disable(if False) the grid.

===============================================================================

## 28. Handling axes


Matplotlib automatically sets the limits of the plot to precisely contain the plotted datasets. Sometimes, we want to set the axes limits ourself. We can set the axes limits with the **axis()** function.

If we execute **axis()** without parameters, it returns the actual axis limits.

We can set parameters to **axis()** by a list of four values. 

The list of four values are the keyword arguments [xmin, xmax, ymin, ymax] allows the minimum and maximum limits for X and Y axis respectively.


We can control the limits for each axis separately using the `xlim()` and `ylim()` functions.

===============================================================================

## 29. Handling X and Y ticks

Vertical and horizontal ticks are those little segments on the axes, coupled with axes labels, used to give a reference system on the graph. So, they form the origin and the grid lines.

Matplotlib provides two basic functions to manage them - **xticks()** and **yticks()**.

Executing with no arguments, the tick function returns the current ticks' locations and the labels corresponding to each of them.

We can pass arguments(in the form of lists) to the ticks functions. The arguments are:-

1. Locations of the ticks

2. Labels to draw at these locations.

===============================================================================

## 30. Adding labels

Another important piece of information to add to a plot is the axes labels, since they specify the type of data we are plotting.

===============================================================================

## 31. Adding a title

The title of a plot describes about the plot. Matplotlib provides a simple function **title()** to add a title to an image.  

===============================================================================

## 32. Adding a legend

Legends are used to describe what each line or curve means in the plot. 

Legends for curves in a figure can be added in two ways. One method is to use the **legend** method of the axis object and pass a list/tuple of legend texts.

The above method follows the MATLAB API. It is prone to errors and unflexible if curves are added to or removed from the plot.
It resulted in a wrongly labelled curve.

A better method is to use the label keyword argument when plots are added to the figure. Then we use the legend method without arguments to add the legend to the figure.

The advantage of this method is that if curves are added or removed from the figure, the legend is automatically updated accordingly.

The **legend** function takes an optional keyword argument **loc**. It specifies the location of the legend to be drawn. 

The **loc** takes numerical codes for the various places the legend can be drawn. The most common **loc** values are as follows:-

ax.legend(loc=0)  # let Matplotlib decide the optimal location

ax.legend(loc=1)  # upper right corner

ax.legend(loc=2)  # upper left corner

ax.legend(loc=3)  # lower left corner

ax.legend(loc=4)  # lower right corner

ax.legend(loc=5)  # right

ax.legend(loc=6)  # center left

ax.legend(loc=7)  # center right

ax.legend(loc=8)  # lower center

ax.legend(loc=9)  # upper center

ax.legend(loc=10) # center

===============================================================================

## 33. Control colours

We can draw different lines or curves in a plot with different colours. 

The colour names and colour abbreviations are given in the following table:-

**Colour abbreviation**      **Colour name**

b                               blue

c                               cyan

g                               green

k                               black

m                               magenta

r                               red

w                               white

y                               yellow

There are several ways to specify colours, other than by colour abbreviations:
    
•	The full colour name, such as yellow

•	Hexadecimal string such as ##FF00FF

•	RGB tuples, for example (1, 0, 1)

•	Grayscale intensity, in string format such as ‘0.7’.

===============================================================================

## 34. Control line styles

Matplotlib provides us different line style options to draw curves or plots. 

All the available line styles are available in the following table:

**Style abbreviation**  **Style**

-                   solid line
   
--                   dashed line
   
-.                   dash-dot line
   
:                    dotted line

===============================================================================

## 35. Summary

In this project, I discuss Matplotlib (the basic plotting library in Python) and throw some light on various charts and customization techniques associated with it.

In particular, I discuss Matplotlib object hierarchy, Matplotlib architecture, Pyplot and Object-Oriented architecture. I also discuss subplots which is very important tool to create graphics in Matplotlib.

Then, I discuss various types of plots like line plot, scatter plot, histogram, bar chart, pie chart, box plot, area chart and contour plot. 

Finally, I discuss various customization techniques. I discuss how to customize the graphics with styles. I discuss how to add a grid and how to handle axes and ticks. I discuss how to add labels, title and legend. I discuss how to customize the charts with colours and line styles.

===============================================================================

## 36. References

The ideas and concepts in this project are taken from the following websites and books:-

i.	Matplotlib official documentation

ii.	https://jakevdp.github.io/PythonDataScienceHandbook/04.00-introduction-to-matplotlib.html

iii.	Matplotlib for Python Developers by Sandro Tosi

iv.	Matplotlib Plotting Cookbook by Alexandre Devert

v.	Python Data Visualization Cookbook by Igor Milovanovic





