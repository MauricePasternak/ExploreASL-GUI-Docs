# Module Overview

--- 

The bulk of the information required to process the ASL data is stored within the separate BIDS sidecars by the end of the [BIDS Import](../1_Import/0_Overview.md) module.

However, there are still some "global" parameters that need to be defined in order for ExploreASL to know how to process the data. These parameters address concepts such as:

- Which subjects should be processed at runtime? Which shouldn't?
- What modeling assumptions should be made for the ASL data?
- Do we want to prioritize quality over speed when processing?
- Should DARTEL be used to create between-subject registration templates?
- Should motion correction be performed on the ASL data? If so, what T-value threshold should be used to determine which volumes should be discarded?
- Which atlases should be used to parcellate region-of-interest CBF data?

These parameters are stored in a file called `DataPar.json` which, when created through this module, will be stored under the study root directory.

For a more in-depth explanation of the parameters stored in `DataPar.json`, please refer to the ExploreASL backend's [documentation website](https://exploreasl.github.io/Documentation/1.10.0beta/ProcessingParameters/#structural-processing-parameters).

