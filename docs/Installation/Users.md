# User Installation

---


There are essentially 3 components required for ASL Analysis using this software:

- The graphical user interface (GUI) software itself (this program)
- An ExploreASL version (compiled or from GitHub)
- A MATLAB version (regular or MATLAB Runtime)

Let's cover the steps for getting each one:

## GUI

Simple enough, head on over to the [**Releases**](https://github.com/MauricePasternak/ExploreASL-GUI/releases) page on the GitHub repository of this GUI and download the version of your preference. The latest version is recommended.

## ExploreASL

There are 2 versions of ExploreASL available:

- From GitHub
- Compiled

These will be referenced regularly within the GUI itself, so be sure to know which one you're using.

### From GitHub

Getting the GitHub one is straight forward. Head on over to the [**ExploreASL repository**](https://github.com/ExploreASL/ExploreASL) and either use the `git` command line tool to clone the repository via command:

```bash
git clone https://github.com/ExploreASL/ExploreASL.git
```

Or download the repository as a ZIP file by clicking the green `Code` button and selecting `Download ZIP`.

<img src="../../assets/img/Installation/ExploreASLGithub_WebPage.png" />

### Compiled

Getting the compiled version is not as straight forward. You will need to contact the <a href="mailto:ExploreASL.LAB@gmail.com" target="_blank">ExploreASL team</a> and request a copy of the compiled version. Be sure to take note which MATLAB version was used to create this compiled package.

## MATLAB

There are 2 versions of MATLAB available:

- Regular
- MATLAB Runtime

### Regular MATLAB

This is a requirement if you are using the GitHub version of ExploreASL. You can download the latest version of MATLAB from the [**MathWorks website**](https://www.mathworks.com/products/matlab.html).

### MATLAB Runtime

This is a requirement if you are using the compiled version of ExploreASL. You can download MATLAB Runtime from the [**MathWorks website**](https://www.mathworks.com/products/compiler/matlab-runtime.html). Be sure to download the version that matches the version of MATLAB used to compile the ExploreASL package.