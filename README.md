# Machine learning techniques for asserting cellular damage induced by particle high-LET radiation
This is a pilot study concerning the use of Machine Learning (ML) techniques for ascertaining the effect of particle ionizing irradiation to cell survival and DNA damage. Our main goal, is to create a ML-based prediction model of the characteristic radiobiological α and β coefficients of the basic Linear Quadratic (LQ) model and several key metrics that quantify DNA damage. The LQ model, is the most common way to associate the response of a population of cells that are 2
being irradiated with the radiation dosage. The surviving population follows the S=e^(- αD - βD ) mathematical equation in a semilogarithmic scaled graph in relation to the dosage measured in Grays (Gy). Our main effort, is to develop a computational prediction framework that will be able to assess key radiobiophysical quantities without sacrificing their interactive nature, and on the other hand to interpret biophysically to the best extent the model and its predictions. Complex DNA damage is calculated using original publicly available datasets using the fast Monte Carlo simulation code (MCDS). MCDS provides metrics that relate to the quantity and distribution of DNA double strand breaks (DSBs) in a genome, something which is widely accepted to be closely related to cell survival and more broadly to the pernicious biological effects of IR and even more in the case of particle irradiation. We critically discuss the varying importance of physical parameters like ion atomic number (Z), charge, linear energy transfer (LET) and the uncertainties of our predictions as well as future directions and the dynamic of our approach. Our endeavor is to produce a ML prediction model that can take into consideration the intrinsic complexities and stochastic effects produced by the interaction of the particle ionizing radiation with biological tissues. Current empirical models do not always take into account such interactions, thus our work will provide a useful prediction algorithm and an interpretation framework in the case of exposure to particle radiations.

## Setup
  - ### Data
      To run the notebook, the dataset needed is provided by [Particle Irradiation Data Ensemble](https://www.gsi.de/work/forschung/biophysik/forschungsfelder/radiobiological_modelling/pide_project.htm) (PIDE v3.2) is required.
  - ### Conda Installation & Python packages:
      Quick summary to install conda and setup the python environment(recommended steps for using python3.x)

    1. wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh -O miniconda.sh
    2. bash miniconda.sh -b -p \$HOME/miniconda
    3. export PATH="\\$HOME/miniconda/bin:\$PATH"
    4. conda config --set always_yes yes --set changeps1 no
    5. conda info -a

    #### Managing conda environment 

    1. create: conda create -n skater-test python=3.6
    2. activate: source activate skater-test
    
    #### Packages
       - conda install numpy==1.17.4
       - conda install scipy==1.5.2
       - conda install matplotlib==3.1.1
       - conda install pandas==0.25.3
       - conda install category_encoders==2.2.2
       - conda install scikit_learn==0.23.2
       - conda install statsmodels==0.12.0
       - conda install xldr
       - conda install jupyter
       - conda install -c conda-forge Skater
  - run 'jupyter notebook' in the same folder where notebook.ipynb lives.
