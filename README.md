# Highly Comparative Time-Series Analysis Demo for CSYS5040
## Tuesday 17 September, 2024

### Google Colab Notebook Link

Please access the Jupyter notebook at: [https://drive.google.com/file/d/1cYMEdBIuAPpO-5OQoFhP34RvgsZ-cMre/view?usp=drive_link](https://drive.google.com/file/d/1cYMEdBIuAPpO-5OQoFhP34RvgsZ-cMre/view?usp=drive_link).
This will open a tab within Google Drive; to run the Jupyter notebook in Google Colab, please save a copy of the `.ipynb` file to your Google Drive and open it.
This should automatically open the file in a Google Colab instance, which will allow you to compile the code and view the outputs directly from your browser without installing anything on your computer.

### Background

Today we will be exploring time-series analysis with two comprehensive libraries in python: 
1. [catch22](https://pypi.org/project/pycatch22/) (a subset of [hctsa](https://github.com/benfulcher/hctsa))
2. [pyspi](https://pypi.org/project/pyspi/)

We'll be working with neuroimaging time-series from a case study described in our original [pyspi publication](https://www.nature.com/articles/s43588-023-00519-x). 
Briefly, this entails resting-state functional magnetic resonance imaging (fMRI) data, which approximates neural activity over time based on hemodynamic coupling.
Typically, researchers will extract time series from parcellated cortical and subcortical brain regions, and will then focus either on local dynamics or pairwise coupling:

![Intra vs. Inter-regional properties in fMRI](https://github.com/anniegbryant/CSYS5040_Demo/blob/main/intra_vs_inter_regional_properties.png?raw=true)

From these time series, we can then summarise properties of local dynamics with hctsa and properties of pairwise coupling between brain regions using pyspi:

![hctsa vs. pyspi](https://github.com/anniegbryant/CSYS5040_Demo/blob/main/time_series_features_types.png?raw=true)

In the original [pyspi publication](https://www.nature.com/articles/s43588-023-00519-x), we asked how well each of 237 statistics for pairwise interactions (SPIs) in pyspi could distinguish fMRI scans obtained while participants were at rest (i.e., chilling in the scanner not actively performing a task) vs. while viewing a film.
We found several SPIs that made this distinction with statistically significant accuracy, many of which surpassed the more typically used Pearson correlation coefficient:
![fMRI case study from pyspi paper](https://github.com/anniegbryant/CSYS5040_Demo/blob/main/pyspi_figure3_fMRI.png?raw=true)
