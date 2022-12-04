# Home

## What is ExploreASL GUI?

This is a graphical user interface (GUI) meant to guide researchers and clinicians in their processing of arterial spin labeling (ASL) scans from the raw DICOM output MRI scanners to the exporting of figures and plots of cerebral blood flow (CBF) data.

## What are the goals of this program?

- To provide a performant and user-friendly experience in ASL processing without requiring any knowledge of programming or having to write error-prone configuration files.

- To facilitate collaboration and communication between neuroscience groups by having their ASL datasets processed in the same semi-automatic manner that is robust to multicenter and multisequence complications that would otherwise arise. To this end, the program explicitly enforces the novel [**ASL-BIDS extension**](https://www.nature.com/articles/s41597-022-01615-9).

- To minimize the probability of any user error perpetuating into a mistaken data-processing error, thereby reducing the amount of discarded neuroimaging data that enters statistical & machine-learning analyses.

    - Every step of this program features validation of user input.

    - Every validation gives user <span style="color: red; font-weight: bold">color</span> & text feedback as to the nature of the error as well as suggestions for ameliorating said error, where appropriate.

- To promote [reusable components](https://reactjs.org/) and sensible programming logic that may be used by other neuroscience-focused developers, either in writing their own tools _de novo_ or migrating their existing codebase for various purposes, such as "modernizing" the look & feel of their applications.

## Pipeline Overview

The user interface divides the processing of ASL data into 5 sections:

<ol>
    <li>DICOM data coming off different MRI scanners and sites must be translated into a consistent BIDS format.</li>
    <li>Imported data should be inspected by the user as a convenient dataframe that allows for adding/deleting/editing BIDS fields for every ASL scan.</li>
    <li>For a given dataset, global parameters are defined regarding variables such as which subjects to process, CBF quantification modeling, which atlases to use for ROI analysis, etc.</li>
    <li><a href="https://www.sciencedirect.com/science/article/pii/S1053811920305176?via%3Dihub">The ExploreASL pipeline</a> is executed on the study in a parallel-processing manner. Specific steps or entire modules can be re-run at any level (subject, scan, etc.)</li>
    <li>Users load regional CBF values from a processed study, merge it with any clinical metadata they may have, and plot it. Interacting with the plot datapoints loads in point-specific CBF image volumes for streamlining quality-control</li>
</ol>

<img src="assets/img/ExploreASL-GUI-Pipeline.png" alt="ExploreASL-GUI Pipeline Flowchart"></img>
