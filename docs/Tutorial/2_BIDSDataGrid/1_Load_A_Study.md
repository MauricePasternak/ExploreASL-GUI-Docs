# Loading a Study

---

Loading in a study is as simple as specifying the path to the study's root directory. The program will then automatically detect the BIDS structure of the study and load all the relevant information to be presented in spreadsheet form:

<img src="../../../assets/img/Tutorial/BIDSDataGrid/1_Load_A_Study/BIDSDG_LoadedInDataframe.png" />

## What is loaded in?

At minimum, the spreadsheet will always contain the following two columns:
- `ID`: This is the spreadsheet's index ID. It is used to keep track of the row's position in the spreadsheet.
- `Filename`: This is the name of the ASL BIDS sidecar that a particular row corresponds to.

These two columns are essential to the functionality of the spreadsheet and thus cannot be modified or removed.

The rest of the columns are automatically generated based on the information present in the BIDS sidecars. The following is a list of all the columns that can be generated:

Note that the names presented here are [**BIDS names**](https://bids-specification.readthedocs.io/en/stable/glossary.html). The spreadsheet will display the names in a more user-friendly format. 

- **Numeric Fields**
	- `BackgroundSuppressionNumberPulses`
	- `BolusCutOffDelayTime`
	- `EchoTime`
	- `FlipAngle`
	- `InversionTime`
	- `LabelingDuration`
	- `MagneticFieldStrength`
	- `M0Estimate`
	- `M0_GMScaleFactor`
	- `PostLabelingDelay`
	- `RepetitionTimePreparation`
	- `TotalAcquiredPairs`
	- `TotalReadoutTime`
- **Text Fields**
	- `PulseSequenceDetails`
	- `ReceiveCoilName`
	- `ScanningSequence`
	- `SequenceName`
	- `SequenceVariant`
	- `SoftwareVersions`
- **Enum Fields**
	- `ArterialSpinLabelingType`
	- `BolusCutOffTechnique`
	- `CASLType`
	- `Manufacturer`
	- `M0Type`
	- `MRAcquisitionType`
	- `PASLType`
	- `PCASLType`
	- `PulseSequenceType`
	- `PhaseEncodingDirection`
	- `SliceEncodingDirection`
- **Boolean Fields**
	- `BackgroundSuppression`
	- `BolusCutOffFlag`
	- `SkullStripped`

In future updates for BIDS fields will be included. However, for 99% of the cases, the above fields should be sufficient to use with ExploreASL.