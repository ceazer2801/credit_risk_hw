# Credit Risk
Week 11 homework assignment

---

## __Data Processing__
To prepare the data I decided to run a for loop through the dataset looking for columns containing string data not including our _target_ column.  For each column containing string data, I performed the `LabelEncoder()` function on the column data and transformed it into integers.

The data was then split into test and train sets and run through a series of models.

---
## __Oversampling__
*Takes the smaller of the feature/target dataset and 'over' samples it until it is the same size as the larger dataset*

### Native Random Oversampling
Native random oversampling gave us a balanced accuracy score of 71 with an f1 score of 81.

### SMOTE
SMOTE gave me slightly worse results than the NRO above with an accuracy score of 70 and an equal f1 score.

---
## __Undersampling__
*Takes the larger of the feature/target dataset and drops data until the sample is the same size as the smaller dataset*

### Cluster Centroids
The cluster centroids was an even worse model for this application with a balanced accuracy score of 64 and an f1 score of 65

---
## __Combination Sampling__
*First takes an oversampling of the smaller dataset, then an undersampling of the larger dataset to even them both*

### SMOTEEN
SMOTEEN has a similar result to SMOTE with a balance score of 69, f1 score of 81

---
## __Ensemble Learners__

### Balanced Random Forest Classifier

The random forest classifier had a higher balanced accuracy score with a mid-range f1 score of 74

### Easy Ensemble Classifier

The easy ensemble classifier has the highest balanced accuracy score with a 93 and an f1 score of 97 with the best fit for this application.