# README

## Introduction
This is my solution to Kaggle's Titanic challenge. I do some exploratory data analysis on the titanic dataset and then transform and clean the data based on this analysis. The data is fitted with a random forest (using ```scikit-learn```'s ```RandomForestClassifier```). I use the out-of-bag (OOB) error as an approximation to the expected new data error. The model is optimised to reduce this error and hence increase the model's ability to generalise to new data and hopefully achieve a better final score!

The original data is included in ```data/train.csv``` and ```data/test.csv```. The data analysis is performed in ```data_analysis.ipynb```, the model is fitted in ```data_fitting.ipynb```, and the final predictions can be found in ```predictions.csv```.

## Installation
1. Ensure you have Conda and Jupyter installed.
2. Clone the repository
   ```sh
   git clone https://github.com/owenhdiba/Kaggle-Titanic.git
   ```
3. Move into the newly created directory of the repo. 
4. Install the conda environment:
   ```sh
   conda env create -f environment.yaml
   ```
5. Activate the environment with 
   ```sh
   conda activate titanic
   ```
6. Add a Jupyter kernel for this environment
   ```sh
   python -m ipykernel install --user --name=titanic --display-name titanic
   ```
## Usage
Running the ```data_analysis.ipynb``` notebook, will load, clean and export the training and test data to the files ```data/train_cleaned.csv``` and ```data/test_cleaned.csv```. Running the ```data_fitting.ipynb``` notebook will load the cleaned data, optimise hyperparameters, and export the test set predictions to the file ```predictions.csv```.
