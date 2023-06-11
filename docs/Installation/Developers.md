# Developer Installation

---

This section is for developers who want to contribute to the development of the software. If you are a user, please refer to the [User Installation](../Installation/Users.md) section.

As with the user installation, there are 3 components required for working with this software:

- The graphical user interface (GUI) software itself (this program)
- An ExploreASL version (compiled or from GitHub)
- A MATLAB version (regular or MATLAB Runtime)

Instructions for obtaining the latter two were outlied in the [User Installation](../Installation/Users.md#exploreasl) section.

## Prerequisites

Before fetching the source code for the GUI, you will need to install the LTS version of [Node.js](https://nodejs.org/en/). This is because the GUI's backend uses Node.js to run the ExploreASL pipeline.

In addition, you will need a package manager for getting all the dependencies for the GUI. The GUI uses [Yarn](https://yarnpkg.com/) as its package manager. You can install Yarn via the [installation instructions](https://classic.yarnpkg.com/en/docs/install/#windows-stable) on their website.

## Downloading the Source Code

Instead of heading over to the Releases page on the GitHub repository of this GUI, you will need to clone the repository via command:

```bash
git clone https://github.com/MauricePasternak/ExploreASL-GUI.git
```

## Installing/Updating Dependencies

Once you have the source code, you will need to install all the dependencies for the GUI.

First navigate to the directory where you cloned the repository:

```bash
cd path/to/ExploreASL-GUI
```

Then install all the dependencies:

```bash
yarn install
```

**:information_source: NOTE:** If you are pulling an updated version of the GUI from `dev` or `main`, you will need to run this command again to update the dependencies.

## Running the GUI

Once you have the dependencies installed, you can run the GUI via command:

```bash
yarn start
```

And that's it! You should now be able to see the GUI running on your computer as two windows: one for the GUI itself and the console/debugger window for assistance with development.

As you make changes to the source code, the GUI will automatically reload. Note that this only applies to changes made to the frontend UI portion. Changes to the backend will require you to close the GUI and restart it for code changes to be reflected.

## Packaging/Deploying the GUI

If you want to package the GUI for distribution, you can do so via command:

```bash
yarn make
```

This will create a folder in the root directory of the repository called `out`. This folder will contain:

- A folder called `ExploreASL-GUI-win32-x64` (or `ExploreASL-GUI-linux-x64` if you are on Linux or `ExploreASL-GUI-darwin-x64` if you are on MacOS) that contains the GUI executable and all the necessary files to run the GUI.
- A folder called `make` that contains the distributable installers for the GUI (i.e. .deb, .exe, .dmg).

## A Note about the Project's Structure

The GUI's complexity requires a certain level of organization to keep things manageable. The following is a brief overview of the project's structure and how it is organized:

```txt
/---|
    |-> assets (media such as icons)
    |-> backend (logic executed by electron's IpcMain, i.e. spawning subprocesses to run ExploreASL)
    |-> common -|
    |           |-> schemas (form validators & form schemas)
    |           |-> types (reusable types & typescript declarations)
    |           |-> utilityFunctions (reusable functions for reducing code use)
    |           |-> GLOBALS.ts (global variables used throughout)
    |
    |-> components (reuseable React components)
    |-> ipc (logic for type-safe IpcMain <-> IpcRenderer communication)
    |-> pages (non-reuseable React components that make up the pages of the GUI)
    |-> stores (frontend-only collections of user-interface state)
    ... other files relate to project setup, package-handling, etc.
```