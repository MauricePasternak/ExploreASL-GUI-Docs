# Rerunning A Study

---

As with re-defining the `dataPar.json` file, sometimes it is necessary to re-run the ExploreASL pipeline. To do so, it is first necessary to indicate the modules/subjects/sessions/steps that are to be re-run.

This can be achieved by clicking on the `Prepare a Re-Run` tab located at the top of this module. You will be greeted with an input field for the study root folder for which you'd like to perform a re-run on.

:exclamation: **Note** :exclamation: 

You cannot re-run a study that is currently being processed. If you attempt to do so, you will be greeted with the following error message:

<img src="../../../assets/img/Tutorial/RunEASL/RunEASL_ReRun_StudyAlreadyRunning.png">

Once you have specified the study root folder (and verified that the study is not currently being processed), you will be greeted with the following view:

<img src="../../../assets/img/Tutorial/RunEASL/RunEASL_ReRun_ExampleSelection.png">

The "tree-view" items here directly correspond to the folders/files found under `derivatives/ExploreASL/lock`. To indicate a re-run, simply select the items that you'd like to have re-evaluated and click the button at the bottom of the screen.

You can then proceed back to the `Run ExploreASL` tab and re-run that study.