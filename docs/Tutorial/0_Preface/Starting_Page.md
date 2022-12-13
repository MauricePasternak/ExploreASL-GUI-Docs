# Starting Page

---

## Overview

When you start up ExploreASL-GUI, you will be greeted with the following screen:

<img src="../../../assets/img/Tutorial/Preface/Starting_Page/Preface_GUI_StartingPage.png" />

This is the About Page. It contains information about the program, some rephrasing of what is mentioned in this documentation, links and contacts, etc.

## Toolbar

The toolbar is located at the top of the GUI. It contains the following buttons:

<img src="../../../assets/img/Tutorial/Preface/Starting_Page/Preface_GUI_Toolbar_Explained.png" />

For a more modern look, you can toggle a dark theme to keep the GUI in sync with your operating system. When you restart the GUI, this choice will be remembered.

Agnostic to operating system, the GUI's window controls (minimize, maximize, close) are located in the top right corner of the GUI. Apologies to the MacOS users for whom this is a deal-breaker.

And finally, to navigate to the different pages of the GUI, there is a menu/navigation toggle located in the top left corner of the GUI.

## Navigation

Toggling the navigation menu will open a sidebar drawer that contains links to the different pages of the GUI:

<img src="../../../assets/img/Tutorial/Preface/Starting_Page/Preface_GUI_Navigation_Menu.png" />

Each link corresponds to a different section/focus of the GUI. In a nutshell:

- **`Import a Dataset`**, for importing your data from DICOMs to NIfTI files
- **`Define Parameters`**, for defining the plethora of parameters that ExploreASL uses to process your data
- **`Edit BIDS Sidecars`**, for fine-tuned adjustments to the BIDS sidecars that are generated during the import process, allowing you to specify the exact parameters that apply for a particular scan, as these may have been missed by the import process due to overly-liberal anonymization procedures.
- **`Process Studies`**, for analyzing your imported and adjusted data in a multiprocessing fashion
- **`Data Visualization`**, for visualizing your processed ASL dataset in combination with your own metadata (i.e. demographics, clinical data, etc.)

With all of this in mind, let's proceed to import our data into NIftI format.