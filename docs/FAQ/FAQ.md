# FAQ

> I don't have previous experience with ASL-MRI analysis. Where can I go to learn more?

There is an excellent ASL overview from the creators of BASIL (an alternative to this program) [**on their documentation page**](https://asl-docs.readthedocs.io/en/latest/analysis_guide.html). Come back here after you've read that.

Okay, now that you understand the basics of ASL, you should be made aware that ASL imaging has been incorporated into a brain imaging standard known as [**BIDS**](https://bids-specification.readthedocs.io/en/stable/). This program revolves around the [**ASL-BIDS extension**](https://www.nature.com/articles/s41597-022-01615-9) whose specification [**is available in online format**](https://bids-specification.readthedocs.io/en/stable/04-modality-specific-files/01-magnetic-resonance-imaging-data.html#arterial-spin-labeling-perfusion-data).

Once you have given yourself a look at the above resources, you should feel more familar with the terminology that will be used by this program and the variety of inputs & labels that are found within it. If you haven't visited the tutorial section of this documentation, you are encouraged to do so by clicking [**here**](../../Tutorial/Preface).

> I don't have a MATLAB license. Can I still use this program?

Yes, but you will need to contact the <a href="mailto:ExploreASL.LAB@gmail.com" target="_blank">ExploreASL team</a> to request a compiled version of ExploreASL that does not require an official MATLAB program on your system. However, you will still need to have a [**MATLAB Runtime**](https://www.mathworks.com/products/compiler/matlab-runtime.html) installed on your system. The particular version depends on the version of MATLAB that was used to compile the ExploreASL program. When you contact the ExploreASL team, they should be able to indicate which version of MATLAB Runtime you will need.

> I have ideas for new features or issues with this program. Where can I go to share these ideas/concerns/questions/etc.?

This program is open source and is hosted on Github. Please see the [**Issues**](https://github.com/MauricePasternak/ExploreASL-GUI/issues/new/choose) page to submit a Bug Report or Feature Request. If you are not familiar with Github, you can also contact the <a href="mailto:maurice.pasternak@utoronto.ca" target="_blank">developer of the program</a> to share your ideas/concerns.

Note: This is primarly for issues associated with the graphical user interface (GUI), not with the "backend" ExploreASL program. While it can be difficult to differentiate the origin of issues that arise (i.e. was it the GUI that failed or is it an issues with ExploreASL), a general rule of thumb is that if there is a message that appears with reference to a folder location of **"derivatives/ExploreASL"**, then it is likely an issue with ExploreASL itself. If there is no such message, then it is likely an issue with the GUI.

