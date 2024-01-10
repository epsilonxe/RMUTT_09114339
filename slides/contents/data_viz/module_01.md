# Module 1

<div class="h-box">Introduction to Visualization Tools</div>


## Learning objectives

In this lesson you will learn about:

- Data visualization and some of the best practices to keep in mind when creating plots and visuals.
- The history and the architecture of Matplotlib.
- Basic plotting with Matplotlib.
- The dataset on immigration to Canada, which will be used extensively throughout the course.
- Generating line plots using Matplotlib.   


## Introduction to Data Visualization


### Why build visuals?
1. For exploratory data analysis (EDA)  
1. Communicate data clearly
1. Share unbiased representation of data
1. Use them to support recommendations of different stakeholders


### Best practices
When creating a visual, always remember:
1. **Less** is more *effective*
1. **Less** is  more *attractive*
1. **Less** is more *impactive*


### Example
<div class="r-stack">
<img class="fragment fade-out current-visible" src="./figures/pie_ex_01.png" data-fragment-index="0">
<img class="fragment fade-out current-visible" src="./figures/pie_ex_02.png">
<img class="fragment fade-out current-visible" src="./figures/pie_ex_03.png">
<img class="fragment fade-out current-visible" src="./figures/pie_ex_04.png">
<img class="fragment fade-out current-visible" src="./figures/pie_ex_05.png"> 
<img class="fragment fade-out current-visible" src="./figures/pie_ex_06.png"> 
<img class="fragment fade-out current-visible" src="./figures/pie_ex_07.png"> 
<img class="fragment fade-out current-visible" src="./figures/pie_ex_08.png"> 
<img class="fragment fade-out current-visible" src="./figures/pie_ex_09.png"> 
<img class="fragment fade-out current-visible" src="./figures/pie_ex_10.png"> 
<img class="fragment fade-out current-visible" src="./figures/pie_ex_11.png">
</div>


### Comparison
<div class="container">
<div class="col">
Before
<img  src="./figures/pie_ex_01.png">
</div>
<div class="col">
After
<img  src="./figures/pie_ex_11.png">
</div>      
</div>


## Introductoion to matplotlib


### History 
<div class="container">
<div class="col">
<img src="figures/matplotlib.png" height=200><br>
John D. Hunter<br>(1968-2012)
</div>
<div class="col">
<img src="figures/ecg.webp" height=200><br>
EEG/ECoG Visualization Tools
</div>
<div class="col">
<img src="figures/matlab.png" height=200><br>
Analogous to MATLAB scripting interface
</div>
</div>


### matplotlib Architecture
<img class="r-stretch" src="figures/matplotlib_architecture.svg">


### Backend layer

It has 3 built-in abstract interface classes:

1. `FigureCanvas`: **matplotlib_backend_bases.FigureCanvas**
    - Encompass the area onto which the figure is drawn
1. `Renderer`: **matplotlib_backend_bases.Renderer**
    - Known how to draw on the FigureCanvas
1. `Event`: **matplotlib_backend_bases.Event**
    - Handles user inputs such as keyboard strokes and mouse clicks


### Artist layer
- Comprised of one main object, i.e.,  **Artist**:
    - Known how to use the `Renderer` to draw on the canvas
- Title, lines, tick labels, images, all correspond to individual **Artist** instances
- Two types of **Artist** objects:
    - Primitive: `Line2D`, `Rectangle`, `Cicle` and `Text`
    - Composite: `Axis`, `Tick`, `Axes` and `Figure`
- Each composite artist may contain other composite artists as well


### Putting the Artist layer to use
<pre class="python">
<code data-line-numbers="1-2,5-6| 10-12" data-trim>
from matplotlib.backends.backend_agg import FigureCanvasAgg as FigureCanvas
from matplotlib.figure import Figure
import numpy as np

fig = Figure()
canvas = FigureCanvas(fig)

x = np.random.randn(10_000)

ax = fig.add_subplot()
ax.hist(x, 100)
fig.savefig('hist.png')
</code>
</pre>


### Output
<img class="r-stretch" src="figures/artist_hist.png">


### Scripting layer
- Comprised mainly of **pyplot**, a scripting interface that is lighter than the **Artist** layer
- Let's see how we can generate the same histogram of 10,000 random values using the **pyplot** interface

<pre class="python">
<code data-trim data-line-numbers="1,5-7">
import matplotlib.pyplot as plt
import numpy as np

x = np.random.randn(10_000)
plt.hist(x, 100)
plt.savefig('hist.png')
plt.show()
</code>
</pre>


### Basic plotting

<pre class="python">
<code data-trim data-noescape data-line-numbers>
import matplotlib.pyplot as plt

plt.plot(5, 8, 'o')
plt.xlabel('x')
plt.ylabel('y')
plt.title('Plotting Example')
plt.show()

</code>
</pre>

<img class="r-stretch" src="figures/plot_ex_01.png">


### matplotlib & pandas

<pre class="python">
<code data-trim>
country_df.plot(kind='line')
</code>
</pre>

<div class="container">
<div class="col">

**country_df**
<br>
<img class="r-stretch" src="figures/country_df.png">    
</div>
<div class="col" style="flex: 3;">
<img src="figures/ex_country_plot.png">
</div>
</div>


### matplotlib & pandas

<pre class="python">
<code data-trim>
country_df['india'].plot(kind='hist')
</code>
</pre>

<div class="container">
<div class="col">

**country_df**
<br>
<img class="r-stretch" src="figures/country_df.png">    
</div>
<div class="col" style="flex: 3;">
<img src="figures/ex_country_hist.png">
</div>
</div>
