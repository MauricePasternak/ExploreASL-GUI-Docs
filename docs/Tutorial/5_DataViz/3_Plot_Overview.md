# Plotting and Interactivity Overview

---

Upon data type clarification, the plotting module will fully open and you will be greeted with the following view:

<img src="../../../assets/img/Tutorial/DataViz/3_Plot_Overview/DataViz_Plot_LandingPage.png">

The plotting module is divided into three main sections:
- The main plot area
- The plot controls
- The MRI views (seen below the main plot area)

## Plot Controls

<img src="../../../assets/img/Tutorial/DataViz/3_Plot_Overview/DataViz_Plot_PlotControlParts.png">

These 4 panels govern the behavior of this module. In summary:
- `Plot Variables`, where you specify the type of plot to be displayed (scatterplot for continuous x continuous, swarmplot for categorical x continuous, etc.)
- `Subsetting Settings`, where you can subset the data by several criteria in order to focus on a specific series of subjects/visits/sessions/scans
- `MRI View Controls`, for controlled the slices displayed for a loaded MRI volume
- `Swarm Plot Visuals` or `Scatter Plot Visuals`, where you can personalize the appearance of the plot (i.e. labels, grid line thickness, etc.)

## Plot Variables

<img src="../../../assets/img/Tutorial/DataViz/3_Plot_Overview/DataViz_Plot_PlotVariables.png">

The `Plot Variables` panel controls the nature of the plot and the data that is displayed. Several inputs are available:

- `Graph Type`:
    - `Scatterplot`: Continuous x Continuous data analysis
    - `Swarmplot`: Categorical x Continuous data analysis
- `X Axis`: Which column to use for the x-axis. Selections are dependent on the `Graph Type` selected.
    - If the `Graph Type` is `Scatterplot`, then the `X Axis` can be any continuous data type column.
    - If the `Graph Type` is `Swarmplot`, then the `X Axis` can be any categorical data type column.
- `Y Axis`: Which column to use for the y-axis. For the time being, this can only be a continuous data type column, as both plot types use continuous values for their dependent (y) variable representation.
- `Color`: An optional column that is only available if the `Graph Type` is `Scatterplot`. This column is expected to be categorical data that will separate data points into different color groups, the levels of which will be displayed in a legend generated on the right side of the plot.
- `Additional Hover Data`: As the plots are interactive, you can hover over data points to see their not only the x and y values, but also any additional columns that you specify here. By default, if this field is left blank, the hover data that is displayed over each data point will include:
    - The Subject/Visit ID
    - The Session ID
    - The X and Y values
    - The color group (if applicable)

---

The remaining plot controls will be covered in their own sections (see below). For now, let's proceed to rendering a basic scatterplot.

- [Scatter Plot Visuals](./4_Scatter_Plot.md)
- [Swarm Plot Visuals](./5_Swarm_Plot.md)
- [MRI View Controls](./6_MRI_View.md)
- [Subsetting Settings](./7_Data_Subsetting.md)