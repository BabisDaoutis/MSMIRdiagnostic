# MSMIRdiagnostic

This is a mid-infrared dianostic for indetifying main sequance star-forming galaxies.

An SVM-based,3-dimensional using custom-defined bands in the 5.9-22 $\mu$m for mid-IR spectra for all observstories.

Repository for galaxy activity classifier from the paper "Mid-Infrared diagnostics for identifying main sequence galaxies in
the local Universe"\
Astronomy & Astrophysics\
ArXiv: TBD \
ADS: TBD \
Publisher (A&A): TBD \

**Authors:**\
C. Daoutis, A. Zezas and M. L. N. Ashby

### Abstract 
**Context.**   \
**Aims.**   \
**Results.**  \
**Conclusions.** 

### Application of the model

This repository includes all the necessary files and a Jupyter notebook as an example of application. The weights of the pre-trained algorithm for implementing the algorithm described in the referenced paper is the 'DONHa_classifier.sav'. We have provided a test file named 'test_sample_galaxies.csv' to verify that your code is functioning correctly. To classify the activity of galaxies in your own catalog, simply replace this test file with your catalog. Supported formats for your catalog are 'fits' or 'csv'.

- **Output of classifier**\
Once the model has been applied to your galaxy catalog, a new column labeled 'classification' will show each galaxy's activity class. The classification labels are encoded numerically, with each number representing a distinct activity class. Below is a legend explaining the meaning of these numerical codes. \
**Classification legend** \
0 - Pure star forming \
1 - Pure AGN \
2 - Pure passive \
3 - Starburst-AGN \
4 - AGN-starburst \
5 - Starburst-passive \
6 - Passive-starburst \
7 - Passive-AGN \
8 - AGN-passive \
-1 - Inconclusive (no result) 
  
For more detailes about the definition of each activity class see Table 3 of the paper. 

Given the significant dependency on specific versions of Python packages, we recommend that users create a conda environment where all required packages are installed according to the versions with which this code has been successfully tested. Detailed instructions for creating the appropriate conda environment are provided below:

**Option 1:**
Run the *environment.yml* file:
```
cd <your-install-dir>
git clone https://github.com/BabisDaoutis/DONHaClassifier.git
cd DONHaClassifier
conda env create -f environment.yml
```
This will create a new conda environment with all the needed python packages.

**Option 2:**
In case there are issues running the *environment.yml*, you can run the following commands in a terminal one by one:

```
conda create --name DONHaclassifier python==3.12.4
conda activate DONHaclassifier
conda install scikit-learn==1.5.1
conda install numpy==1.26.4
conda install astropy==6.1.0
conda install matplotlib==3.8.4
conda install pandas==2.2.2
conda install jupyter notebook
```
