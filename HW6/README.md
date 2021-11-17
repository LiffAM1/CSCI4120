# CSCI 4120 - Group 8 - Homework 6
**Group Members:** 
Abigail Holloway, hollowayab21@students.ecu.edu
Nicholas Everette, everetten17@students.ecu.edu

This README file will walk you through how to run our Homework 6 Jupyter notebook, which uses PCA and SVM to classify digits and tunes hyperparameters for the SVM model.

## Dependencies

The following dependencies and packages are required to be installed on the host machine in order to run the script:
 - Python (>= 3.5)
 - Jupyter
 - Juptyer Notebooks
 - yellowbrick
 - seaborn
 - pandas
 - random
 - math
 - numpy
 - sklearn
 - matplotlib

## Walkthrough

1. Use Git command line or a Git UI to clone the repo (https://github.com/LiffAM1/CSCI4120_Group8.git)
2. In a terminal, cd to the directory where you cloned the repo to.
3. Run the command 'jupyter notebook' to start jupyter. Click on the HW5_RandomForest.ipynb file to open it.
4. Run the notebook by pressing 'Run'.

## Results
In order to keep 80% of the information, we need about 12 principal components. By creating pipelines with this PCA model and the three SVM kernels (linear, poly, and rbf), we find the following results when running 5 fold cross validation:
- Linear best parameters: {'svc__C': 10}
- Linear test set accuracy: 0.9577777777777777
- Poly best parameters: {'svc__degree': 3, 'svc__C': 100}
- Poly test set accuracy: 0.9755555555555555
- RBF best parameters: {'svc__gamma': 0.001, 'svc__C': 100}
- RBF test set accuracy: 0.9822222222222222

From this we can clearly see that RBF is the best kernel to use for this problem (which can be guessed by visualizing the data). The best hyperparameter values to use for the RBF kernel are gamma = 0.001 and C = 100.
