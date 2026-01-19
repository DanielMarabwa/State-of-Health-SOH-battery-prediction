# State-of-Health-SOH-battery-prediction
The State of Health (SOH) of a battery indicates how its current capacity compares to when it was new. For example, if a battery originally lasted 10 hours but lasts only 7 hours after two years of use, its SOH is 70%. In this project, researchers simulated battery usage over time, and machine learning models are used to predict SOH.

## State of Health (SOH) Derived Forumla 

In this project, the SOH formula is derived because the original researchers did not explicitly calculate the SOH values.

The SOH is calculated as:

**SOH** = (Cap(W) / Cap(i)) × 100%

Where:
- **Cap(W)**: Battery capacity at cycle *W* (after a certain number of charge and discharge cycles)
- **Cap(i)**: Initial battery capacity when the battery was new
- A **cycle** refers to one complete charge and discharge process of a battery. In other words, when a battery is used from 100% down to 0% and then charged back to 100%, one full cycle is completed.

## Data

The data used in this project comes from the NASA Battery Data Set. Lithium-ion batteries underwent charging, discharging, and impedance cycles continuously until they reached End-of-Life (EOL) criteria, defined as a 20% to 30% fade in rated capacity. Data from these experiments was recorded and stored in MATLAB files. Please refer to the **MATLAB Data Description** (under the **Battery Data** section) for further details.

A data collection process, implemented in Python, was used to extract the battery data from the original MATLAB files, transform it into useful features, and convert it into a dataframe and a CSV file. Please refer to **"Extracted Features and Explaination of Data"** (under the **"Battery Data"** section) for further details.

Original data set link: https://www.nasa.gov/intelligent-systems-division/discovery-and-systems-health/pcoe/pcoe-data-set-repository/

Download: https://phm-datasets.s3.amazonaws.com/NASA/5.+Battery+Data+Set.zip

Data Set Citation: B. Saha and K. Goebel (2007). “Battery Data Set”, NASA Prognostics Data Repository, NASA Ames Research Center, Moffett Field, CA

## Code

The code is split into 3 parts that are not intergrated. 

**Part 1: Explore Matlab Battery Data Structure.ipynb** 

Prerequisites: Battery **B0005.mat** (under the **Battery Data** section)

This notebook conducts an exploratory analysis of Matlab battery data. This aids in understanding the data structure of the battery files.

**Part 2: Data Cleaning.ipynb** 

Prerequisites: All 29 batteries (under the **Battery Data** section)

This notebook converts 29 Matlab battery files into a DataFrame and then a CSV file (**"Battery_input_features_updated.csv"**). Seventeen features are extracted by aggregating the battery-related data.

**Part 3: EDA and Model Build.ipynb** 

Prequisties: **Battery_input_features_updated.csv**

In this notebook, the modeling process is split into two parts: pre-optimization and post-optimization. Pre-optimization means that we take the dataset and do not implement any exploratory data analysis (EDA) in order to evaluate the baseline performance of the model. Post-optimization means that we apply feature engineering (deriving new features), EDA, outlier removal, grid search, and backward elimination to the dataset before passing the data through the model. Three models were built and trained using both the pre-optimization and post-optimization approaches.



