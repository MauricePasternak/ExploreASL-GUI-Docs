# Adding BIDS Fields

---

To begin adding a BIDS field that isn't currently present in the spreadsheet, click on the `Add Column` button located in the spreadsheet's toolbar.

<img src="../../../assets/img/Tutorial/BIDSDataGrid/3_Adding_BIDS_Fields/BIDSDG_AddingAColumn_Part0.png" />

This will open a modal window that will prompt you to select a field to be added to the spreadsheet.

<img src="../../../assets/img/Tutorial/BIDSDataGrid/3_Adding_BIDS_Fields/BIDSDG_AddingAColumn_Part1.png" />

For example, let's add the `Skull Stipped` field. After selecting a field, the appropriate input will be displayed below the field name (i.e. numeric input for numeric fields, another dropdown for enum fields, etc.). This will allow you to enter the value for the field for all the rows in the spreadsheet.

<img src="../../../assets/img/Tutorial/BIDSDataGrid/3_Adding_BIDS_Fields/BIDSDG_AddingAColumn_Part2.png" />

Alternatively, there will be a second option presented where you can opt to populate all the rows for that column with blank values. This is particularly useful if you want to add an exclusionary field for a complex dataset where 99% of the subjects shouldn't have the field but the remaining 1% should. It would be otherwise tedious to manually delete all the values for that field.

<img src="../../../assets/img/Tutorial/BIDSDataGrid/3_Adding_BIDS_Fields/BIDSDG_AddingAColumn_Part3.png" />

For the purposes of this tutorial, we will opt to make this "mistake" and populate all the rows with blank values. After pressing `Add to Spreadsheet`, the field will be added to the spreadsheet:

<img src="../../../assets/img/Tutorial/BIDSDataGrid/3_Adding_BIDS_Fields/BIDSDG_AddingAColumn_Part4.png" />

**NOTE** This added column will always be found at the **rightmost end** of the spreadsheet.