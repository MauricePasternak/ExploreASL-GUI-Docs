# ExploreASL Processing Parameters

---

This section will cover control over the different behaviours of submodules within the ExploreASL pipeline, which include:

- Structural Module; for processing anatomical data into a template space
- ASL Module; for processing ASL & M0 data into CBF volumes
- Population Module; for generating population statistics from the processed data

## General Processing Parameters

These are meta parameters that generally affect processing time as well as memory & disk usage.

- `Processing & Image Quality` - Controls the quality and precision of the processing. An approximate 5-fold increase to the processing time is expected when using the higher quality setting (~20-30 min for a single subject with a single visit & scan).
- `Handling of Folders & Missing Scans` - Self-explanatory. The default settings (see below) are to save on disk space but avoid skipping scans where at least some partial processing can be done.

<img src="../../../assets/img/Tutorial/DataPar/3_ProcPars/DataPar_ProcPars_General.png" />

## Structural Module Parameters

<img src="../../../assets/img/Tutorial/DataPar/3_ProcPars/DataPar_ProcPars_Structural.png" />

See the [ExploreASL documentation](https://exploreasl.github.io/Documentation/1.10.0beta/ProcessingParameters/#structural-processing-parameters) for more information on these parameters.

## ASL Module Parameters

<img src="../../../assets/img/Tutorial/DataPar/3_ProcPars/DataPar_ProcPars_ASL.png" />

See the [ExploreASL documentation](https://exploreasl.github.io/Documentation/1.10.0beta/ProcessingParameters/#asl-processing-parameters) for more information on these parameters.

## Population Module Parameters

<img src="../../../assets/img/Tutorial/DataPar/3_ProcPars/DataPar_ProcPars_Population.png" />

See the [ExploreASL documentation](https://exploreasl.github.io/Documentation/1.10.0beta/ProcessingParameters/#masking-atlas-parameters) for more information on these parameters.

:exclamation: **IMPORTANT NOTE** :exclamation:

If no atlases are specified, then it will not be possible to use the Data Visualization module of this software, as no CBF ROI statistics will be generated. Ensure that you research which atlas(es) are important for your study and check what is appropriate.

