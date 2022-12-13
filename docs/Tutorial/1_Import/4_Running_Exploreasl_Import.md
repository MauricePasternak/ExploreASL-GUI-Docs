# Running the ExploreASL Import Module

---

This page is relatively straightforward. It is simply a text feedback field coupled with buttons to control the execution (Pause, Resume, Stop) of the import process. At the current time, the text feedback is direct output from the ExploreASL program.

Simply click `Run ExploreASL Import Module` in the bottom right corner of the GUI to start the import process. The GUI will then look like this:

<img src="../../../assets/img/Tutorial/Import/4_Run_Import_Module/Import_RunImportModule_Controls.png" />

And when complete, you will receive a message to take a look at the generated `rawdata` and `derivatives` folders, in particular the log files from the ExploreASL process, in order to verify that all expected images were imported over. In a future update, this part will be more automated to give better feedback regarding import errors, if any occurred.

We now have a BIDS-compliant dataset:

<img src="../../../assets/img/Tutorial/Import/4_Run_Import_Module/Import_RunImportModule_FinishedRun.png" />

---

As part of the import validity verification, in the next step we will be looking at the BIDS sidecars that were generated during the import process. To proceed, toggle the navigation menu and select `Edit BIDS Sidecars`.