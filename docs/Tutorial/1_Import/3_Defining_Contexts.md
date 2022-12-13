# Define Contexts

---

## What is a context?

A "context" here refers to the particular unique settings that defines a grouping of ASL image acquisitions. Factors like which vendor, scanner, sequence, labeling strategy, number of control-label pairs, etc. are all factors that can be used to define a context. Goodness willing, you will only have to define one context if your dataset is relatively simple (i.e. single scanner at a single site). However, for complex datasets, it is likely that you will have to define multiple contexts.

## What are the contexts here?

In the example dataset, we have three different contexts:

<img src="../../../assets/img/Tutorial/Import/3_Define_Contexts/Import_DefineContexts_FolderToContextRelation.png" />

1. Subjects 001 and 002 were acquired on a GE scanner with a 3D Spiral sequence and PCASL labeling.
2. Subject 003 was acquired on a Siemens scanner with 3D GRASE sequence and PASL labeling, and output as 20 DICOMs representing 10 control & label pairs.
3. Subject 004 was acquired on a Siemens scanner with PASL labeling, and output as 60 DICOMs representing an averaged control & label pair.

Despite being called "Global Context", it won't apply to the entire dataset if other contexts (like in this case) are present. It will only apply to the subjects/visits/sessions that are NOT specified in some other context.

## Parts of a context

For the most optimal processability, the program will require information about the following aspects of your data:

- `ASL Context`: what does the ASL data look like (i.e. is it a control-label alterating series, a pre-processed perfusion image, etc.)?
- `M0 Scan Information`: is there an M0 scan, and if so, where is it located? Or should a numerical estimate be used instead?
- `Additional ASL Information`: properties like the scanner's manufacturer, ASL labeling type, etc.
- `Background Suppression Information`: is there background suppression, and if so, what are the timings?

### ASL Context

The ASL Context is a mandatory set of fields that, together, allows the program to understand the nature of the ASL data. Otherwise, it would be tedious to manually specify what each volume in an ASL timeseries represents, especially if it consists of many volumes with embedded dummy scans.

The fields to fill out are:

- The ASL Series Pattern: A general template to understand the type of ASL data present. Options include:
    - `Alternating Control, Label Series`: This is the most common type of ASL data. It is a series of alternating control and label volumes, with the first volume being a control volume.
    - `Alternating Label, Control Series`: This is the same as the previous option, but with the first volume being a label volume.
    - `Intermediate Perfusion Weighted Image`: This is a pre-processed difference image between the control and label volumes.
    - `Complete Perfusion (CBF) Image`: This is a pre-processed CBF image.

- Number of Volumes in the ASL Series: The number of volumes present overall in the series, inclusive of dummy and M0 scans that may be present.

- M0 Positions within ASL Series: The locations, as numbers separated by commas, of where embedded M0 scans are located within the ASL series. If there are no M0 scans, leave this field blank. 1 is the first volume in the series.

- Dummy Scan Positions within ASL Series: Same logic as the previous field, but for dummy scans.

For the example dataset, where we are leaving the GE data as the "global" context, we have knowledge that the first volume (of 2) is a perfusion weighted (difference) image, and the second volume is the M0 scan. So we fill out the fields as follows:

<img src="../../../assets/img/Tutorial/Import/3_Define_Contexts/Import_DefineContexts_ASLContext.png" />

### M0 Scan Information

These are the fields that allow the program to understand where the M0 scan is located, and how it should be processed. The fields to fill out are:

- M0 Type: The nature of the M0 scan itself. Options include:
    - `Separate`: The M0 scan is a separate acquisition from the ASL scan. It is **not** embedded within the ASL series.
    - `Included`: The M0 scan is embedded within the ASL scan.
    - `Estimate`: The M0 scan is not present, and in its place a numerical estimate should be used.
    - `Absent`: The M0 scan is not present, and no numerical estimate should be used (not recommended).
- M0 Estimate: If the previous field is set to `Estimate`, then this field is required. It is the numerical value that will be used in place of the M0 scan in CBF quantification.

### Additional ASL Information

These are fields that allow the program to understand the properties of the ASL data. The fields to fill out are:

- Manufacturer: The manufacturer of the scanner that acquired the data. Options include:
    - `GE`
    - `Philips`
    - `Siemens`
- ASL Sequence Type: The sequence used to acquire the data. Options include:
    - `2D EPI`
    - `3D Spiral`
    - `3D GRASE`
- Labeling Type: The type of ASL labeling strategy used. Options include:
    - `PCASL`
    - `PASL`
    - `CASL`
- Post Label Delay: For PASL scans or GE 3D Spiral sequences, the value to use is that of TI (inversion time). For (P)CASL scans, it is the time between the end of the labeling period and the start of the MRI acquisition.
- Labeling Duration: The duration of the labeling pulse, in milliseconds. This should be left alone at zero if the labeling type is `PASL`
- Bolus Cut-Off Flag: This is the PASL-only field that indicates whether the bolus cut-off technique was used (recommended for accurate quantification of PASL data).
- Bolus Cut-Off Technique: This is the PASL-only field that indicates the type of bolus cut-off technique used. Options include:
    - `QUIPSS`,
    - `QUIPSSII`,
    - `Q2TIPS`
- Bolus Cut-Off Delay Time: This is the PASL-only field that indicates the timings used to define the labeling period. For Q2TIPs, the field change to 2 timings for the first and last bolus cut-off pulses, respectively.

### Background Suppression Information

These are fields that assist with correcting for the effect of background suppression on the ASL data. The fields to fill out are:
- Number of Background Suppression Pulses: The number of background suppression pulses present in the ASL scan.
- Background Suppression Pulses Timing: The timings of the background suppression pulses, in seconds, separated by commas.

Here is an example of the fields filled out for the GE "global context" data:

<img src="../../../assets/img/Tutorial/Import/3_Define_Contexts/Import_DefineContexts_M0ASLandBSInfo.png" />


### Additional Context - Specifying Subsets

Each "Additional Context" interface has an extra field featuring a filepath dropzone for identifying which subjects/visits/sessions are to be treated with that context.

<img src="../../../assets/img/Tutorial/Import/3_Define_Contexts/Import_DefineContexts_AdditionalContextDropzone.png">

Note that folders that were earlier specified as `Ignore` or `Scan` when defining the dataset structure will not be allowed in the dropzone.

### Reloading upon revisit

Since this step is by far the most tedious, a series of configuration files are saved at the study root folder:

<img src="../../../assets/img/Tutorial/Import/3_Define_Contexts/Import_DefineContexts_SuccessfulSubmit.png">

These will be used to auto-reload the contexts if this step is revisited for the same study. Note that this assumes that the dataset structure has not changed since the last time the step was completed.

---

Once all the contexts have been defined, click `Next` in the bottom right corner to proceed to the next step.

