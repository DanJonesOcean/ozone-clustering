# Ozone clustering in UKESM1
Here we use Gaussian mixture modelling as implimented in the scikit-learn python package to classify ozone profiles in the UKESM1 model. We train the model using annual mean profiles from:

1. The historical simulation from 2004-2014

2. SSP126 from 2090-2100

3. SSP585 from 2090-2100

![image](https://user-images.githubusercontent.com/11757453/116451791-d9d0ef80-a854-11eb-89a6-6c1874e23415.png)

By training the GMM using a combined dataset with profiles from (1)-(3) we ensure that the GMM captures a wide variety of profile types across the forcing scenarios. We then label the profiles separately and examine how the class properties change over time and with forcing scenario.

This repository contains:

* bic : a plot of the BIC score with number of classes to guide selection of N
* classes-n : collections of plots and statistical models using 'n' classes
* data_in : both the NetCDF data extracted from UKESM1 and the same data formatted as CSV
* get_UKESM_ozone_profiles : the script used to extract ozone profiles from UKESM1 on Pangeo
* Ozone profile clustering : notebook containing the fitting and labeling of classes

![image](https://user-images.githubusercontent.com/11757453/116451823-e5241b00-a854-11eb-80a0-cf98f1fc8127.png)
