[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/lab-biotek-bio-ugm/BIC30007-2/HEAD)
# BIC30007-2
Modul Praktikum Bioinformatika 2022 - Fakultas Biologi UGM.
- [Modul 2](acara_02/)
- [Modul 7](acara_07/)

## Usage
### Step 1: Clone the repository

[Clone](https://help.github.com/en/articles/cloning-a-repository) this repository to your local system.

    git git@github.com:lab-biotek-bio-ugm/BIC30007-2.git
    cd BIC30007-2
    
### Step 2: Install dependencies

You can install the necessary dependencies from [`environment.yml`](environment.yml) by using either Conda or [Mamba](https://github.com/mamba-org/mamba), which is advised. You can install [Mamba](https://github.com/mamba-org/mamba) into any other Conda-based Python distribution with:

    conda install -n base -c conda-forge mamba

Then install the dependencies with:

    mamba create env -f environment.yml

### Step 3: Run Jupyter Lab

Activate the environment via:

    conda activate bic30007-2022
    
Then start Jupyter Lab:

    jupyter lab