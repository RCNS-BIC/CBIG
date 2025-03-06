# MRI economics: Balancing sample size and scan duration in brain wide association studies (ME)
# REFERENCE
* Ooi LQR*, Orban C*, Zhang S*, Nichols TE, ..., Yeo BTT. [MRI economics: Balancing sample size and scan duration in brain wide association studies](https://www.biorxiv.org/content/10.1101/2024.02.16.580448v2). bioRxiv, 2024. 

# BACKGROUND
A pervasive dilemma in neuroimaging is whether to prioritize sample size or scan duration given fixed resources. Here, we systematically investigate this trade-off in the context of brain-wide association studies (BWAS) using resting-state functional magnetic resonance imaging (fMRI). 

![MRI Economics Figures](./readme_figures/README_Figure.jpg)

We show that sample size and scan duration are broadly interchangable below 30 minutes. We explain the influence of sample size and scan duration with a theoretical model. Finally, we investigate how accounting for costs impacts study design.
Our online calculator is available [here](https://thomasyeolab.github.io/OptimalScanTimeCalculator/index.html).

# CODE RELEASE
## Download stand-alone repository
Since the whole Github repository is too big, we provide a stand-alone version of only this project and its dependencies. 
To download this stand-alone repository, visit this link: [To be updated upon acceptance](https://github.com/ThomasYeoLab/Standalone_Ooi2024_ME)

## Download whole repository
Except for this project, if you want to use the code for other stable projects from our lab as well, you need to download the whole repository.

To download the version of the code that was last tested, you can either visit this link: 

[https://github.com/ThomasYeoLab/CBIG/releases/tag/v0.34.0-Ooi2024_ME](https://github.com/ThomasYeoLab/CBIG/releases/tag/v0.34.0-Ooi2024_ME)

run the following command, if you have Git installed

```
git checkout -b Ooi2024_ME v0.34.0-Ooi2024_ME
```

# USAGE
## Setup
1. Make sure you have installed: Matlab 2018b and the python environment here `$CBIG_CODE_DIR/stable_projects/predict_phenotypes/Ooi2024_ME/replication/config/Ooi2024_ME.yml`
2. Follow `$CBIG_CODE_DIR/setup/README.md` to setup the config file. Instead of using `$CBIG_CODE_DIR/setup/CBIG_sample_config.sh`, you need to use `$CBIG_CODE_DIR/stable_projects/predict_phenotypes/Ooi2024_ME/replication/config/CBIG_ME_tested_config.sh.` and modify `ME_rep_dir` within the file according to your desired output directory.
3. To use the same data, for the ABCD data, please ensure you have access to ABCD through the NDA website in study [Link to be updated](Update_this). For the HCP data, the HCP repository is publicly available. However, please apply for restricted access to the HCP to gain access to information such as age and the Family ID.


## Replication
* `replication`: This folder contains wrapper scripts to replicate all the analyses in this paper. Also contains a config folder which contains the software requirements and packages to replicate the results.

## Prediction and reliability analyses
* `Prediction`: this folder contains the scripts and workflows to generate prediction results using KRR and LRR.
* `Reliability`: this folder contains the scripts to generate the univariate and multivariate reliability results.

## Curve fitting
* `curve_fitting`: This folder contains scripts to fit the logarithmic and theoretical models to the prediction accuracy and reliability results in the previous step.

## Figure plotting
* `figure_plotting`: This folder contains scripts to generate figures found in the paper.

## Examples and unit tests
* `examples`: this folder provides a toy example for running the regression code and fitting the logarithmic and theoretical models.
* `unit_tests`: this folder runs codes in `examples` and checks the reference output.

# UPDATES
Release v0.34.0 (06/03/2025): Initial release of Ooi2024_ME

# BUGS and QUESTIONS
Please contact Leon Ooi at leonooiqr@gmail.com and Thomas Yeo at yeoyeo02@gmail.com.
