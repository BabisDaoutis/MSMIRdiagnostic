# MSMIRdiagnostic

This is a mid-infrared dianostic for indetifying main sequance (MS) star-forming galaxies.

An SVM-based,3-dimensional using custom-defined bands in the 5.9-22 μm for mid-IR spectra for all observstories.

Repository for galaxy activity classifier from the paper "Mid-Infrared diagnostics for identifying main sequence galaxies in
the local Universe"\
Astronomy & Astrophysics\
ArXiv: TBD \
ADS: TBD \
Publisher (A&A): TBD 

**Authors:**\
C. Daoutis, A. Zezas, and M. L. N. Ashby

### Abstract 
**Context.** A galaxy’s mid-infrared spectrum captures a significant amount of information about its internal conditions such as the
radiation field strength and its star formation activity. It is also intricately connected to dust characteristics and it contains spectral
lines that serve as crucial indicators for galaxy activity diagnostics. Thus, characterizing galaxies’ mid-infrared spectra is highly
constraining of their nature. \
**Aims.** This project describes a diagnostic tool for identifying main-sequence star-forming galaxies in the local Universe using infrared
dust emission features that are characteristic galaxy activity. \
**Methods.** A physically motivated sample of mock galaxy spectra has been generated to simulate the infrared emission of star-forming
galaxies in the local Universe. Using this sample, we developed a diagnostic tool for identifying main-sequence star-forming galaxies
with machine learning methods. Custom photometric bands were defined to target key dust emission features, including polycyclic
aromatic hydrocarbons (PAHs) and the dust continuum. Specifically, three bands were selected to capture PAH emission peaks at
6.2 µm, 7.7 and 8.6 µm, and 11.3 µm, along with one band that estimated the strength of the radiation field that illuminated the dust.
This diagnostic was subsequently applied to observed galaxies to evaluate its eﬀectiveness in real-world applications. \
**Results.** Our diagnostic achieves high performance scores, accurately identifying 90.9% of main-sequence star-forming galaxies in a
sample of observed galaxies. Additionally, it demonstrates low contamination, with only 16.2% of AGN galaxies being misidentified
as star-forming based on our test sample. \
**Conclusions.** It is possible to combine observational studies and stellar population synthesis (SPS) frameworks to generate physically
motivated simulated samples of star forming galaxies that exhibit similar spectral properties as their observed counterparts. By strate-
gically positioning custom photometric bands on the mid-infrared spectrum to target specific dust emission features, our diagnostic
can extract valuable information without the need to measure specific emission lines. Although PAHs are sensitive indicators of star
formation and interstellar medium (ISM) radiation hardness, PAH emission alone is insuﬃcient for identifying main-sequence star-
forming galaxies. Finally, we have developed a physically-motivated spectral library of main sequence star-forming galaxies spanning
from ultraviolet to far-infrared wavelengths.

### Application of the model

This repository contains all the required files and a Jupyter notebook as an example of an application. The weights of the pre-trained algorithm for implementing the algorithm described in the referenced paper is the '**TBD.sav**'. We have provided an example spactrum 'TBD.csv' to verify that your code is functioning correctly.

- **Output of diagnostic**\
After applying the model to a galaxy's spectrum, the diagnostic provides the classification result, indicating whether the galaxy is a main sequence star-forming galaxy or not. \
**Classification legend** \
0 - MS star-forming galaxy \
1 - NON-MS star-forming galaxy \

Given the significant dependency on specific versions of Python packages, we recommend that users create a conda environment where all required packages are installed according to the versions with which this code has been successfully tested. Detailed instructions for creating the appropriate conda environment are provided below:

**Option 1:**
Run the *environment.yml* file:
```
cd <your-install-dir>
git clone https://github.com/BabisDaoutis/MSMIRdiagnostic.git
cd MSMIRdiagnostic
conda env create -f environment.yml
```
This will create a new conda environment with all the needed python packages.

**Option 2:**
In case there are issues running the *environment.yml*, you can run the following commands in a terminal one by one:

```
conda create --name MSMIRdiagnostic python==3.13.0
conda activate MSMIRdiagnostic
conda install scikit-learn==1.5.2
conda install numpy==2.2.2
conda install astropy==7.0.1
conda install matplotlib==3.9.2
conda install pandas==2.2.3
conda install jupyter notebook
```
