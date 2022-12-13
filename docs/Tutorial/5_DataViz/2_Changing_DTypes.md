# Clarifying Data Types

---

When the data has successfully loaded, you will be presented with a table of column names and their detected data types. Data type options include:

- Categorical (or nominal/ordinal data)
- Continuous (or interval/ratio/numerical data)
- Ignore (to exclude a column from further analysis)

<img src="../../../assets/img/Tutorial/DataViz/2_Changing_DTypes/DataViz_SpecifyDatatypes.png" />

Once you have clarified the data types, you can proceed to the next step by clicking on `Go to Plotting` in the bottom right corner of the window.

## Categorical Encoded Data

While it is likely that the majority of the interpretation of columns will be accurate, it is quite often the case that some categorical data may be mis-interpreted by the program as continuous since it is encoded as numbers. By clarifying this earlier, we can allow the program to use these numerically-encoded columns for plots that have a categorical x-axis (i.e. swarmplots).