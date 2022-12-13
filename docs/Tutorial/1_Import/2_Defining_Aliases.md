# Defining Aliases

---

There are two issues we need to resolve here. 

1. Allowing the import pipeline to understand what folder names mean. Our example may have convenient names for scans like "ASL" or "T1", but this is not always the case. Sometimes it may be a random set of characters that is consistent across all subjects/visits/etc.

2. Allowing for renaming from these difficult-to-understand DICOM folder names to more legible and shareable aliases.

## Defining Aliases for Scans

The first problem is tackled when we define aliases for scans. In the earlier step, when we specified which folder depth had "`Scan`"s in it, the program has now gathered the folder names present at that level so that we can define the meaning behind them. The options are as follows:

- `Ignore this Folder`: This option is useful for additional fluff output by the scanner that happens to be present at the same level as the scans.
- `T1 Structural Scans`
- `T2 Structural Scans`
- `FLAIR Structural Scans`
- `ASL Functional Scans`
- `Proton-Density (M0) Scans`

<img src="../../../assets/img/Tutorial/Import/2_Define_Aliases/Import_DefineAliases_ScanAliases.png">

In our example, the mapping is obvious. Again, this is not always the case.

## Defining Aliases for Visits and Sessions

The second problem is tackled by defining aliases for visits and sessions. The same logic applies as for scans: from our earlier step, the program understands the names of folders found at a certain depth away from `sourcedata`. Now it is asking the question "would you like this to be called something else when its imported?".

In our example, this would be advantageous. The folder names of 01 and 02 are not very descriptive of their meaning (i.e. that one is a baseline scan and the other is a followup). Therefore we can specify that these should be called "Baseline" and "Followup" respectively.

<img src="../../../assets/img/Tutorial/Import/2_Define_Aliases/Import_DefineAliases_VisitAliases.png">

You can also see that when a particular piece of information is absent (in our example, Session/Run information), a default description is placed in the position where a mapping input would be.

We can proceed to the penultimate step of the import pipeline.