# Default ASL Sequence & Modeling Parameters

---

## Sequence & Acquisition Parameters

:warning: **Deprecation Warning**: This is a legacy section that will be removed in the next release. :warning: 

Originally, ExploreASL did not incorporate BIDS format into its analysis, and so the many ASL sequence & acquisition related parameters that were identified in the [Import Module](../1_Import/3_Defining_Contexts.md) were originally specified in this section.

<img src="../../../assets/img/Tutorial/DataPar/2_SeqPars/DataPar_SeqPars_ASLAcqPars.png">

Note that this section can still be used to specify fallback values in the event that the import procedure did not extract relevant information from the DICOM headers (i.e. due to excessive anonymization or human errors in scan acquisition).

However, it is more recommended to adjust settings at the scan level using the "Edit BIDS Sidecars" module discussed in an [earlier section](../2_BIDSDataGrid/0_Overview.md).

## Modeling and CBF Quantification Parameters

This section is responsible for specifying the modeling and quantification parameters for extracting CBF values from the ASL data.

<img src="../../../assets/img/Tutorial/DataPar/2_SeqPars/DataPar_SeqPars_CBFQuantPars.png">

Please refer to the [ASL consensus paper](https://pubmed.ncbi.nlm.nih.gov/24715426/), for which the default values shown above are set from (assuming 3T strength acquisition) or the backend [ExploreASL documentation](https://exploreasl.github.io/Documentation/1.10.0beta/ProcessingParameters/#quantification-parameters) for more information on these parameters.
