# Study Project: Adversarial Machine Learning
# Generation of Datasets for Anomaly Detection in Industrial Control Systems

## Part I: Statistical Analysis and Generation of Process Data

The goal of this study project is to first implement different approaches for generating synthetic, but at the same time realistic datasets using artificial intelligence.This part get familiars ICS dataset WADI, analyze the properties of the dataset, and implement our own approach for the generation of synthetic dataset from the original WADI dataset.

## Set Up

Create an isolated environment and install the required data science packages:

```python3 -m venv .venv ``` 

```source .venv/bin/activate ```

The list of dependencies can be found under ```requirements.txt```. 
The following command can be used to install all of them at once: 

``` pip install -r requirements.txt ```.

This project is configured to run out of your user's home directory path structure:
* **Python Path Target:** `Path.home() / "Projects" / "P1"`
* **Ubuntu Terminal Path:** `~/Projects/P1/`

curl command to download the shared WADI datasets:

WADI2017 : WADI_14days.csv

```curl -L -o WADI_14days.csv https://www.b-tu.de/owncloud/s/e9HQmcMBQZj6Kqo```


WADI2017 : WADI_attackdata.csv

```curl -L -o WADI_attackdata.csv https://www.b-tu.de/owncloud/s/x5mFzgJRjjfSjHf```


WADI2019 : WADI_14days_new.csv

```curl -L -o WADI_14days_new.csv https://www.b-tu.de/owncloud/s/4b5atn6WN2j3MHF```


WADI2019 : WADI_attackdataLABLE.csv

```curl -L -o WADI_attackdataLABLE.csv https://www.b-tu.de/owncloud/s/GbscdskgMSF76tP```


## Data Source

This project relies on datasets from WADI (Water Distribution) that are used as benchmark dataset for Industrial Control Systems (ICS) and Cyber-Physical Systems security. Developed by iTrust at the Singapore University of Technology and Design (SUTD), it serves as a scaled-down, highly realistic physical model of a large city's water distribution network. 

Data Source 

WADI: https://sutdapac-my.sharepoint.com/:f:/g/personal/itrust_sutd_edu_sg/EiYnIxyvOdREgo0NjPUI7dcBXDxoGosa37Wkam7xRd4rTQ?e=3neAvd


## Project Directory Structure


```Project Folder
Projects/P1/
├── data/
│   ├── raw/                   # Original datasets and files from WADI
│   │   ├── 2017/              # WADI2017 datasets of 2017
│   │   └── 2019/              # WADI2019 datasets of 2019     
│   └── processed/             # Saved Dataframes from CSV files and Generated Synthetic Data CSV files
│       └── synthetic_data.csv # Generated sample synthetic data CSV file for Task 3
├── notebooks/                 # Jupyter notebooks for quick prototyping and JupyterNotebook PDF output files
├── src/                       # Production-ready Python source code
│   ├── T1.py                  # Python script for Task 1
│   ├── T2.py                  # Python script for Task 2
│   ├── T2_histogram.png       # Generated Histogram PNG file for Task 2b
│   └── T3.py                  # Python script for Task 3      
├── README.md                  # Project description, setup instructions, project folder and directory structure 
└── requirements.txt           # List of project dependencies (pandas, numpy, pyarrow, matplotlib and scikit-learn)
```

---

## Source Code 

Our contribution is organised into several folders and files, based on the role of the code. Here is an outline and short description on the content. Details about the features we implemented are presented as in-line documentation, i.e. in the code files.

- [```src```](src) - Source folder

    - [```T1.py```](src/T1.py) 

    - [```T2.py```](src/T2.py)
      - output generated histogram (T2_histogram.png)

    - [```T3.py```](src/T3.py)
      - output generated synthetic data CSV file (~/Projects/P1/data/Processed/synthetic_data.csv)
      - Input1: select dataset as real sample for generating data
      - Input2: Percentage of dataset for sample (1-100%);
      - Input3: Select Normalize Method (1 or 2);
      - Input4: Percentage of synthetic data (1-1000%);
      - Input5: k of nearest neighbour (2-5).
  
### Submission
+ Date : 28 October 2026
+ Group 15 SIN Wang Yat
