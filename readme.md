# Recurrent Events Analysis With Data Collected at Informative Clinical Visits in Electronic Health Records

# Author Contributions Checklist Form

## Data

### Abstract

The data consists of the electronic health record data of 160 patients
who underwent kidney transplant at the Johns Hopkins Hospital in the
year of 2012. The medical records captured by REDCap (Research
Electronic Data Capture) include all post-transplant visits until
September 24, 2014. By a thorough review of the relevant microbiology
and clinical laboratory data, a total of 199 serious infection episodes
were identified among the 654 clinical visits recorded in the REDCap
database. The data contains information on demographic and clinical
factors at baseline, as well as the creatinine level measured at each
clinical visit.

### Availability

The data is owned by Dr. Kieren Marr’s research group at Johns Hopkins
University. The group is currently working on several other manuscripts
using the same study. Since the study itself represents the major
scientific capital for the group, we do not plan on making the data
publicly available at the moment.

In the R package reVAR, we provide a function genData to simulate
datasets that have the same structure as the kidney transplant data.

## Code

### Abstract

The R package reVAR includes functions to implement the proposed
methods. The package was used to conduct recurrent event analysis on the
kidney transplant data. Version 0.0.1 is available at
<https://github.com/yifeisun/reVAR>.

The vignette for using reVAR can be found in the directory
reVAR/vignettes, where we include detailed instructions on how to
prepare the data and run the analysis.

The code to reproduce the simulation tables are in the directory
reVAR/simulations.

### Description

The package reVAR has the following functions:

-   genData: Generate a simulated dataset under scenarios of the
    simulation studies in Sun et al. (2020+).

-   reVAR: Fit the proportional rate model with intermittently measured
    time-dependent covariates under the visiting at random (VAR)
    assumption.

-   reVARBoot: ﻿Generate bootstrap replicates of the estimates under
    VAR.

-   reVCAR: Fit the proportional rate model with intermittently measured
    time-dependent covariates under the visiting completely at random
    (VCAR) assumption.

-   reVCARBoot: Generate bootstrap replicates of the estimates under
    VCAR.

### Optional Information (complete as necessary)

Dependencies of the package reVAR: NHPoisson (version 3.3); survival
(version 3.1-11); nleqslv (version 3.3.2).

## Instructions for Use

### Reproducibility

***Reproducing the data analysis*** The use of the above functions are
demonstrated in “Example.pdf”, where we use a simulated dataset that has
the same structure as our data example. The vignette shows the steps to
generate Table 3, Table 4, and Figure 2.

***Reproducing the simulation tables*** The functions used in the
simulation studies are in “functions_simulation.R”. The code in
“Table_Sun_et_al_2020.R” was used to generate Table 1 and 2 in the
paper. One can specify the argument sce in the function oneiter to
obtain results for any of the ten scenarios in the simulations: In Table
1, scenarios I-VI correspond to "VCAR1", "VAR2", "VAR3", "VCAR4",
"VAR-M5", "VAR-M6", respectively. In Table 2, scenarios VII-X correspond
to "VNAR7", "VNAR8", "VNAR9", "VNAR10", respectively. Other packages
used in the simulation studies for parallel computing include doParallel
(version 1.0.15); doRNG (version 1.7.1).

### Replication

All functions in the R package are documented with examples.
