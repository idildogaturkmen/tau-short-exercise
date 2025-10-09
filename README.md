# CMS DAS @ Hamburg 2025: Tau Short Exercise

The Tau short exercise is organised in the two Jupyter notebooks contained in this repository.
Please join our [`short-ex-tau` MatterMost channel](https://mattermost.web.cern.ch/cmsdas-2025-desyuhh/channels/short-exercise-tau)
in the [CMSDAS@DESY2025 MatterMost team](https://mattermost.web.cern.ch/signup_user_complete/?id=bfipbmm8i7fm786b9sfj7aqcgy&md=link&sbr=su).
The slides are available [here](https://gitlab.cern.ch/cmsdas-hamburg-2025/tau-short-exercise).

## Recommended way to run the exercise (SWAN)
To run the notebooks with regular CERN resources:
1. Open a SWAN session at https://swan.cern.ch
2. The default settings are good: as of writing you can pick software stack "107" with platform "AlmaLinux 9".
   Older versions will still work provided they include "Python 3" for the exercise.
3. In the SWAN session, click on the download button (cloud with an downward arrow)
   on the right-hand side that says "Download Project from git".
4. Copy-paste this repository: `https://gitlab.cern.ch/cmsdas-hamburg-2025/tau-short-exercise.git` .
5. Now you are all set and can click on the two exercises `tau_short_exercise_*.ipynb`!

### Troubleshooting:
* If you already have a running SWAN session and want to change the settings,
you have to click the ellipsis button (•••) in the top right corner,
and clicking "Change configuration" in the dropdown menu.

## Alternative way to run the exercise (local)
To run the notebooks locally:
1. Install [Python](https://www.python.org/downloads/), [ROOT](https://root.cern/install/) and [Jupyter](https://jupyter.org/install).
2. Open a terminal and create a working directory.
3. Download the package by `git clone https://gitlab.cern.ch/cmsdas-hamburg-2025/tau-short-exercise.git`.
4. Enter the package by `cd tau-short-exercise`.
5. Download the input files from LPC node by `scp -r <USERNAME>@lxplus.cern.ch:/eos/user/c/cmsdas/2024/short-ex-tau .`.
   using your own CERN/lxplus username..
6. You're all set and can launch the two exercises locally, `jupyter-notebook tau_short_exercise_1.ipynb`
   and `jupyter-notebook tau_short_exercise_2.ipynb`, which will open the kernel in your browser.

### Troubleshooting
* The software stack can be installed with brew and/or pip (root, jupyter, python3) locally.
* If the jupyter notebook cannot find ROOT lib link in your laptop despite the above installations,
  you can try with `root --notebook tau_short_exercise_1.ipynb` and `root --notebook tau_short_exercise_2.ipynb`.

## Feedback
If you finished the exercise, it would be great to send your feedback to the
[`short-ex-tau` MatterMost channel](https://mattermost.web.cern.ch/cmsdas24/channels/tau_short_exercise)
with the information whether you were able to successfully tackle the exercise
and ideally also with pointers to finished notebooks, either linked on GitLab,
or made available as exported websites or documents, etc.
At the same time, we'd be very interested in getting specific feedback, suggestions, etc.,
so we can improve the exercise for future usage.

## References
### Papers:
* [TAU-24-001](https://cms-results.web.cern.ch/cms-results/public-results/preliminary-results/TAU-24-001/):
  Latest paper describing the Run 3 version of DeepTau and the calibration performed with 2022 and 2023 data-taking.
* [TAU-20-001](https://cms-results.web.cern.ch/cms-results/public-results/publications/TAU-20-001/index.html):
  Latest paper describing the HPS reconstruction and DeepTau identification algorithms for hadronic tau decays at CMS.
  * Hardon-plus-strips (HPS) is an algorithm that reconstructs the different hadronic decay modes of the tau
    using tracks and calorimeter clusters inside a narrow jet cone.
  * DeepTau is a convolutional neural networks to discriminate jets, muons, and electrons
    that are misidentified as hadronic tau decays.
* [TAU-16-003](http://cms-results.web.cern.ch/cms-results/public-results/publications/TAU-16-003/index.html):
  Previous paper about HPS reconstruction.

### CMS TauPOG:
* Website: https://tau-wiki.docs.cern.ch
* Main TWiki: https://twiki.cern.ch/twiki/bin/view/CMS/Tau
* Regular meetings: https://indico.cern.ch/category/1307/overview?period=week
* Recommendations for Run 2: https://twiki.cern.ch/twiki/bin/view/CMS/TauIDRecommendationForRun2
* Recommendations for Run 3: https://twiki.cern.ch/twiki/bin/view/CMS/TauIDRecommendationForRun3
