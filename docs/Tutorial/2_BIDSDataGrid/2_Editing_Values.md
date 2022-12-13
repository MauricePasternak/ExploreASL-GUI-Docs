# Editing BIDS Values

---

Like Excel, the spreadsheet allows you to edit the values of the cells. Simply double-click the cell of interest and an editor view of that cell will appear with the value focused. You can then edit the value within the confines of what is reasonably permitted for that cell. For example, you cannot enter a letter in a cell that is meant for numbers.

Once you are done editing the value, press `Enter` to save the changes or click elsewhere to have the cell lose focus and auto-submit its value.

**NOTE**: For certain complex fields like `Bolus Cut-off Delay Time` that switch between a number and a collection of numbers, saving values may be somewhat slow (i.e. you press Enter and the previous value remains). This is related to the next section (validation is occurring) and performance improvements are planned. For the time being, if you encounter this, you may need to wait a second for the value to be saveable.

## Making Mistakes

Of course, even within the confines of what is reasonably permitted for a cell, you can still make mistakes that will invalidate the integrity of the data in terms of BIDS specifications. Not to worry, though, as validation is executed as values are submitted. For instance, let us put in an unreasonable value for `Magnetic Field Strength`:

<img src="../../../assets/img/Tutorial/BIDSDataGrid/2_Editing_Values/BIDSDG_MakeError_Part1.png" />

As you can see, the cell is highlighted in red to indicate its invalidity. Furthermore, to keep track of the locations of errors for larger datasets with hundreds of rows, the option to view errors appears in the toolbar. Clicking it will open a small popover window that will list all the errors in the spreadsheet:

<img src="../../../assets/img/Tutorial/BIDSDataGrid/2_Editing_Values/BIDSDG_MakeError_Part2.png" />

## Incompatible Fields

In BIDS, there are cases where certain fields are exclusive to one another. For example, if the `Arterial Spin Labeling Type` is set to `PASL`, then there cannot exist a field of `Labeling Duration` for that same scan/row. But until now we only saw how to change the value of cells to other values. How do we remove a value altogether to say "this cell should be treated as empty"?

<img src="../../../assets/img/Tutorial/BIDSDataGrid/2_Editing_Values/BIDSDG_SelectingSuspiciousValues.png" />

The answer is to select the cell of interest and press the `Delete` key on your keyboard (not `Backspace`!). This will remove the value from the cell and set it to empty.

**NOTE**: On some keyboards, this the `Delete` key is in the shorthand form of `Del` above the arrow keys. 