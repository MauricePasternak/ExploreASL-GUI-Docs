# Reloading Data

---

As in the previous example, sometimes the mistakes we make are not easily reversible and a hard refresh is required. This can be done by clicking the `Reload Data` button in the toolbar.

<img src="../../../assets/img/Tutorial/BIDSDataGrid/5_Reloading_Data/BIDSDG_Reloading_Part1.png" />

This will prompt the program to reload the data from the study again and will reset the spreadsheet to its original state.

<img src="../../../assets/img/Tutorial/BIDSDataGrid/5_Reloading_Data/BIDSDG_Reloading_Part2.png" />

<p style="color: red; font-weight: 800; font-size: 1.5rem">WARNING</p> If, instead of clicking the `Reload Data` button, you were to save the changes made by clicking `Save & Overwrite BIDS Sidecars`, then reloading the data will not undo the changes made. This is because reloading treats the `rawdata` folder as the source of truth.

Only click `Save & Overwrite BIDS Sidecars` if you are sure that your changes are what you want and are in line with BIDS standards. In a measure to be understanding that strange exceptions exist, the option to save changes will remain enabled even when there are BIDS errors present, but the responsibility in then on the user.

## If it all went wrong

Despite the above warning, what can a user do if they saved significant changes that can't be undone easily? Chances are, it would be far more efficient to simply re-run the Import Module and start over rather than editing potentially hundreds of files manually.