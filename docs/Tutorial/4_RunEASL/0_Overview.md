# Module Overview

---

To navigate to this module, toggle ExploreASL-GUI's navigation bar and click the `Run ExploreASL` option found under `Process Studies`.

You should be greeted with the following screen:

<img src="../../../assets/img/Tutorial/RunEASL/RunEASL_LandingPage.png">

This module is responsible for running one or more studies with defined `dataPar.json` files & imported scans simultaneously. By default, the module is set to process only a single study, but you can change this by selecting the appropriate value under the `Select the numer of studies to process` dropdown menu.

For example, by selecting `5` from the dropdown menu, you will be able to process 5 studies simultaneously:

<img src="../../../assets/img/Tutorial/RunEASL/RunEASL_ChangingNumOfStudies.png">

:warning: **Warning** :warning: 

The number of studies you can process simultaneously is limited by the number of CPU cores available on your machine. For example, if you have a 4-core CPU, you will only be able to process 4 studies simultaneously. Attempting to exceed this may result in a crash. Logic to prevent this from happening is in place, but due diligence is still advised.

---

For this tutorial, we will only be processing the single study we imported.