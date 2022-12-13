# Scatterplot

---

## Basic Scatter Plot

At minimum, to render a scatterplot, you must specify the following:
- `Graph Type`: `Scatterplot`
- `X Axis`: Any continuous data type column
- `Y Axis`: Any continuous data type column

The following is an example of a basic scatterplot:

<img src="../../../assets/img/Tutorial/DataViz/4_Scatter_Plot/DataViz_Plot_ScatterPlot_Basic.png">

Initially, not very pretty, but certainly useable for basic data exploration. Let's see how we can make this plot more visually appealing.

## Scatter Plot Visual Settings

The `Scatter Plot Visuals` panel allows you to adjust the appearance of the scatterplot. There are a considerable number of options available which will be summarized below:

<img src="../../../assets/img/Tutorial/DataViz/4_Scatter_Plot/DataViz_Plot_ScatterPlot_Settings.png" />

### Color

- Color Palette: Allows for control over the color palette used when a `Color` column is specified in the `Plot Variables` panel. The default is `Set 1`, but you can also select from a number of other known palettes.

### Markers

- Size: Allows for control over the scatter point marker size.

### Margins

- Left, Top, Right, Bottom: Allows for control over the margins of the plot. This is useful if you want to increase the size of the plot to make it more readable or if other elements are overlapping with the plot.

### Grid Lines

- X Axis, Y Axis: Whether to render grid lines on the x and y axes, respectively.
- Grid Line Width: The thickness of the grid lines.

### X Axis Settings

- X Axis Label: The label for the x axis. Defaults to the column label, but this allows you to override it for a more readable label.
- Tick Height: The length of the ticks protruding from the x axis.
- Tick Width: The thickness of the ticks protruding from the x axis.
- Tick Label Offset: The distance from the x axis to the tick labels.
- Tick Label Rotation: The angle of rotation of the tick labels. This is useful if the tick labels are overlapping with each other.
- Tick Label Font Size: The font size of the tick labels.
- Axis Label Font Size: The font size of the main x axis label/title.
- Axis Label Offset: The distance from the x axis to the main x axis label/title.

### Y Axis Settings

Same as the x axis settings, but for the y axis.

### Legend Settings

- Main Anchor: The anchor point for the legend. This is useful if you want to move the legend to a different location on the plot.
- Legend Direction: The orientation of items within the legend.
- Item Packing Order: The order of items within the legend.
- Translate X: The horizontal offset of the legend from the anchor point.
- Translate Y: The vertical offset of the legend from the anchor point.
- Item Spacing: The spacing between items within the legend.
- Legend Item Width: The width of each item (marker + label) within the legend.
- Legend Item Height: The height of each item (marker + label) within the legend.
- Symbol Size: The size of the markers within the legend.
- Label Font Size: The font size of the labels within the legend.

## Prettified Scatter Plot

Let's see how we can make the scatterplot look a little nicer once the visual settings are adjusted:

<img src="../../../assets/img/Tutorial/DataViz/4_Scatter_Plot/DataViz_Plot_ScatterPlot_Prettified.png">
