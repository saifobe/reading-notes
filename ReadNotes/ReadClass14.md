# Bokeh 

## What is Bokeh?

Bokeh is an interactive visualization library that targets modern web browsers for presentation. It is good for:

- Interactive visualization in modern browsers
- Standalone HTML documents, or server-backed apps
- Expressive and versatile graphics
- Large, dynamic or streaming data
- Easy usage from python (or Scala, or R, or...)

## How to install Bokeh?

```python
pip install bokeh
```

## How to use Bokeh?

```python
from bokeh.plotting import figure, output_file, show

# prepare some data
x = [1, 2, 3, 4, 5]
y = [6, 7, 2, 4, 5]

# output to static HTML file
output_file("lines.html")

# create a new plot with a title and axis labels
p = figure(title="simple line example", x_axis_label='x', y_axis_label='y')

# add a line renderer with legend and line thickness
p.line(x, y, legend_label="Temp.", line_width=2)

# show the results
show(p)
```

## How to use Bokeh with Pandas?

```python
from bokeh.plotting import figure, output_file, show
from bokeh.sampledata.stocks import AAPL
import pandas

df = pandas.DataFrame(AAPL)
df["date"] = pandas.to_datetime(df["date"])

p = figure(plot_width=800, plot_height=250, x_axis_type="datetime")
p.line(df["date"], df["close"], color='navy', alpha=0.5)

output_file("datetime.html")

show(p)
```

## How to use Bokeh with NumPy?

```python
from bokeh.plotting import figure, output_file, show
import numpy as np

# prepare some data
N = 4000
x = np.random.random(size=N) * 100
y = np.random.random(size=N) * 100
radii = np.random.random(size=N) * 1.5
colors = [
    "#%02x%02x%02x" % (int(r), int(g), 150) for r, g in zip(50+2*x, 30+2*y)
]

# output to static HTML file (with CDN resources)
output_file("color_scatter.html", title="color_scatter.py example", mode="cdn")

TOOLS="crosshair,pan,wheel_zoom,box_zoom,reset,box_select,lasso_select"

# create a new plot with the tools above, and explicit ranges
p = figure(tools=TOOLS, x_range=(0,100), y_range=(0,100))

# add a circle renderer with vectorized colors and sizes
p.circle(x,y, radius=radii, fill_color=colors, fill_alpha=0.6, line_color=None)

# show the results
show(p)
```

