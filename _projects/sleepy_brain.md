---
layout: page
title: Classification of Sex and Age Groups from Resting-State Functional Data Using ML
description: Can we classify sex and age based on rs-fMRI?
img: assets/img/sleepy_fmri_age_full_corr.png
importance: 2
category: Other
related_publications:
---
### What we wanted to know
The aim of our project was to apply a previously successful classification method, tangent embedding, to resting-state functional data from The Stockholm Sleepy Brain dataset.
### What we did
In this project, we built upon the [nilearn example's](https://nilearn.github.io/auto_examples/03_connectivity/plot_group_level_connectivity.html) classification of age using functional connectivity. Extending their findings, we applied the tangent embedding classifier to The Stockholm Sleepy Brain resting-state functional data. Our objective was to classify both sex (female vs. male) and age group (young vs. old) using an increased test sample size (n = 10).
### What we found
The finding from the original [nilearn example](https://nilearn.github.io/auto_examples/03_connectivity/plot_group_level_connectivity.html) was not replicated, though our participants were sleep deprived so I'm guessing that was why. We also had a small dataset, as this was a tiny project meant to reproduce some code, not necessarily the result. See code under [respositories](/repositories/) if interested.