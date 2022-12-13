# Saving and Loading Configurations

---

To save or load a `DataPar.json` configuration file, click the `Save` or `Load` button located at the bottom of ExploreASL-GUI's main window.

<img src="../../../assets/img/Tutorial/DataPar/4_Saving_And_Loading/DataPar_SaveAndLoad.png" />

## Saving

After filling in the relevant parameters and clicking the `Save` button, one of two things will happen:

- The save does not occur and invalid fields are marked throughout with red highlights. This is to ensure that the user does not accidentally save an invalid configuration file. Fix these as prompted by the error message hints and try again.

- The save occurs and you receive a confirmation message:

<img src="../../../assets/img/Tutorial/DataPar/4_Saving_And_Loading/DataPar_SaveConfirmation.png" />

We can examine the contents of the configuration file by opening it in a text editor:

<img src="../../../assets/img/Tutorial/DataPar/4_Saving_And_Loading/DataPar_DataParJSON_Example.png" />

And in the event that there is a limitation to the GUI, it is possible to manually edit the fields in. This is not recommended, but can be done if necessary. For more information on the appropriate values to use in each field in the event of manual configuration, please refer to the [ExploreASL documentation](https://exploreasl.github.io/Documentation/1.10.0beta/ProcessingParameters/).

## Loading

It is likely that in the course of your work, you will need to tweak certain parameters in your configuration file. Re-entering all of the parameters manually can be tedious, so it is possible to load a previously saved configuration file and edit the parameters as necessary.

As with saving, after clicking the `Load` button and selecting the `dataPar.json` file located at the study root folder, one of two things will happen:

- The load occurs without warning and all fields are populated with the values from the configuration file.
- The load still occurs, but due to certain fields being invalid (i.e. perhaps BIDS schema has changed, filepaths are no longer valid, etc.), you will be prompted with a warning message detailing which fields were invalid and the particular validation error encountered.

In the example below, filepath fields for the ExploreASL directory and the study root directory were deliberately tampered with to demonstrate the warning message:

<img src="../../../assets/img/Tutorial/DataPar/4_Saving_And_Loading/DataPar_InvalidLoad.png" />

--- 

With the data imported, validated, and global configurations define, we can finally proceed to run the main ExploreASL analysis.