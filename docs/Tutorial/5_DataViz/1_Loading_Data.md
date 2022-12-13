# Loading a Dataset

---

In order for a dataset to be loaded, the following must be specified:

- `Study Root Path`: The filepath to the folder for this analyzed study. This is the folder that, itself, contains the `derivatives`, `rawdata`, and `sourcedata` folders.
- `Metadata Filepath`: (Optional) The filepath to the `.csv` or `.tsv` file containing additional data to merge with the output of ExploreASL. See the [Metadata/Ancillary Information Incorporation](../5_DataViz/0_Overview.md#metadataancillary-information-incorporation) section for more information.
- `Which Atlas Statistic to Load`: Self-explanatory - are we interested in the mean, median, or spatial coefficient of variation (CoV) of the data?
- `Which Partial Volume Correction Spreadsheet to Load`: Self-explanatory - are we interested in the partial volume corrected (PVC) or non-partial volume corrected (non-PVC) data?
- `Atlases to Load`: Which regions of interest based on atlas do we want to have CBF values loaded from. :exclamation: **Note** :exclamation: that you can only load the atlases that were analyzed and indicated earlier when we were defining [ExploreASL's processing settings](../3_DataPar/3_ProcPars.md#population-module-parameters).

<img src="../../../assets/img/Tutorial/DataViz/1_Loading_Data/DataViz_LoadDataFrame.png" />

If performed correctly, clicking on `Proceed to Clarify Data Types` will proceed to the next step.