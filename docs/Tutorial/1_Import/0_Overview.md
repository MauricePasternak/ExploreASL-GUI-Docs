# Import Module Overview

---

In this tutorial, we will be importing our dataset's DICOMs into NIfTI files. This is a necessary prerequisite for the rest of the pipeline.

The necessity for this stems from the consensus of using NIfTI files as the standard format for neuroimaging data analysis by the scientific community.

<p align="center">
    <img src="../../../assets/img/Tutorial/Import/0_Overview/DICOM2BIDS.png" />
</p>

There have been several excellent tools developed for this purpose, such as [dcm2niix](https://github.com/rordenlab/dcm2niix), [dcm2bids](https://github.com/UNFmontreal/Dcm2Bids/issues), among others. Unfortunately, these tools are either not fully automated, or require a significant degree of programming knowledge to use.

ExploreASL-GUI will avoid these caveats by allowing you to specify the meanings of folders found in your dataset and then executing the import process in a fully automated fashion. Of course, the drawback is that your dataset must follow certain rules, which we will discuss in the next section when we look at the first page of the Import pipeline.