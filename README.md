# Folder structure

Data comprises the final normative data frames ready for modelling. There is:
- Details on the scale 36 parcellation ('ROI1'), inc. names, labels, xyz coords, hemisphere, cortical
- The same for the scale 60 parcellation ('ROI2') rqd. for supp. only
- A df with Subj ID / Site / Age / Sex / ROI / RBP in five freq. bands, for ROI1. The main data table.
- The same for ROI2, for supp. only
- The same ROI1 RBP table, but this time symmetric regions are pooled, increasing sample size per region
- The number of sites per region in the pooled ROI1 RBP data
- The number of subject per region in the ROI1 RBP data

Modelling has three modelling scripts:
- Whole brain - model and effect assessment.R is used to determine the optimal fixed effect structure (Methods) and then evaluate the importance of fixed & random effects (Results 3.1-3.3)
- Whole brain - age CIs.R calculates regression coefficients and CIs for the age model (Result 3.4)
- Regional - model and stats.R fits the age model at the ROI level and extracts relevant summaries (Result 3.5)

Output scripts are:
- EDA.R produces the subject distribution visualisation (Methods) and linearity checks (Supp.)
- age_model_ROI_plots.R produces regional-level subplots and plots in Results
- b_age_brain_maps.m produces the brain figure displaying b_age values (Result 3.4)
- strong_ROI_plots_and_wholebrain_CIs.R gives scatter plots of two well-populated ROIs, to 'zoom in' on the model along with whole brain CIs (Result 3.4)
- sup_models.R handles the modelling for supp., results are then run through coefs brain map.m
- sup_age_range.R checks that regional results are not correlated with the region's distribution of ages, for supp.

The MATLAB folder has the functions called to plot the brains along with the pial files needed.

Tracking pngs due to long plotting time.
