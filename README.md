# README FILE FOR DATABYTE TASK 1 ( WINE QUALITY PREDICTION).

Wine Dataset available on UCI Repository is of two categories:

1. Red Wine Dataset and

1. White Wine Dataset.

For DataByte Induction Task We will be working on Red Wine Dataset to explore the Features upon which the quality of the Red Wine depends.
## I HAVE CONVERTED THE RED WINE DATASET INTO EXCEL TYPE FORMAT USING EXCEL SO USE THE DATA PRESENT IN THE REPOSITORY.

THE FLOW OF THE README FILE WILL BE AS FOLLOWS:

1. INSIGHTS OF THE EDA PERFORMED ON THE DATASET.

1. NAIVE BAYES ALGORITHM FROM SCRATCH.

1. DECISION TREE ALGORITHM FROM SCRATCH.

1. BASIC IMPLEMENTATION OF ANN FROM SCRATCH.

1. IMPLEMENTATION OF ANN USING TENSORLOW AND KERAS.

## INSIGHTS OF THE EDA PERFORMED

From the EXPLORATORY DATA ANALYSIS Performed on the Dataset, we get to know the very accurate analysis of the Data.

1. SHAPE OF THE DATA:
  
(1599, 12)


  ### So there are 1599 Data points in the dataset, each described by 12 features including the label.

2. FEATURES IN THE DATASET:
   
![](   
https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/EDA/36503272-8652-40ed-ae77-a283e7f3132f.png?raw=true)

DETERMINING THE NULL VALUES AND DATA TYPES:

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/EDA/Screenshot%202023-07-15%20012840.png)

STATISTICAL INSIGHTS:

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/EDA/08b718c5-24d9-4adf-bbb8-813743845b88.png?raw=true)

array([3, 4, 5, 6, 7, 8], dtype=int64)

CLASS IMBALANCE:

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/EDA/4e0653ac-d7bb-4cb7-a645-3c92af3e43e4.png?raw=true)

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/EDA/e9d21736-cd6d-4aed-8af1-2bb83f8e3072.png?raw=true)

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/EDA/2235fee4-ee5d-48cd-aafc-69d4f4a68795.png?raw=true)

BY LOOKING AT THE GRAPHS WE CAN FIND THE SPREAD OF THE FEATURES AND ALSO WE GET TO KNOW THAT FEATURES HAVE OUTLIERS AS WILL BE PROVED FROM THE BOX PLOT OF EACH FEATURE AS

MATHEMATICAL INTERPRETATION OF OUTLIERS(Z-SCORES: Z-score is a way to standardize the data to a standard scale i.e. how far the data point is from the mean.)

NUMBER OF OUTLIERS PER CLASS.
![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/EDA/bc59c680-670f-4f2b-b912-967c43649cb9.png?raw=true)

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/EDA/c47e251c-e3bd-4cd7-b091-4df247b2d99c.png?raw=true)

THEN WE GO FOR BIVARIATE ANALYSIS FOR FINDING THE DEPENDENCIES BETWEEN THE FEATURES OF THE DATASET, BY PLOTTING PAIR-WISE PLOT. BY THIS WE GOT TO KNOW THAT THERE ARE ONLY A FEW FEATURES WIHIC IS RELATED THIS IS THE CAUSE FOR WHICH THE NAIVE BAYES MODEL OUTPERFORM THE DECISION TREE MODEL.

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/EDA/a937fac5-1d4e-415e-94cb-b8b5a70ad722.png?raw=truea)

THROUGH ALL THIS WE GOT TO KNOW:

1. THE DATASET HAS 1599 POINTS AND 12 FEATURES

1. 6 CLASS LABELS

1. DATASET IS ALSO IMBALANCED

1. DATASET CONTAINS APPROX 11 PERCENT OUTLIERS.

1. THERE IS VERY LESS CORRELATION BETWEEN THE FEATURES.

1. THE CHLORIDE CLASS HAS MAXIMUM OUTLIERS.

1. CITRIC ACID HAS MINIMUM OUTLIERS.

1. AS THE ALCOHOL CONTENT INCREASES QUALITY INCREASES.

1. VOLATILE ACIDITY HAS THE MAXIMUM NEGATIVE IMPACT ON THE WINE QUALITY.

1. FREE SULPHUR CONTENT HAS THE LEAST IMPACT ON THE WINE QUALITY.

1. ANALYSIS OF DIFFERENT MODELS IMPLEMENTED ON THE DATASET:

# NAIVE BAYES:

## ACCURACY: 61.25%

### CONFUSION MATRIX:

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/NAIVE%20BAYES/4072f32a-9175-41e7-9fa1-ac0e9c381e5b.png?raw=true)

BY CONFUSION MATRIX WE GET TO KNOW THAT CLASS 5 AND 6 ARE THE ONES FOR ACCURACY IS LOW BUT THEY HAVE HIGHER PRECISION i.e. WHEN OUR MODEL PREDICT SOME POINT AS 5 THEN MORE THAN 60% SURE THAT IT IS CORRECT AND ALSO WHEN OUR MODEL PREDICT SOMR POINT AS 5 OUT ALL THE CORRECT CLASSES THEN IT MORE THAN 65% SURE THAT POINTS PREDICTED AS 5 ARE CORRECT. SIMILARLY, F1_SCORE IS JUST THE HARMONIC MEAN OF THE RECALL AND PRECISION.

THE FOLLOWING GRAPHS ILLUSTRATE THE EVALUATION OF THE MODEL ON DIFFERENT PARAMETERS CONCERNING CLASS LABELS.

CLASSWISE ACCURACY

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/NAIVE%20BAYES/f638926b-f8ad-4a55-8116-e704ea39bdd6.png?raw=true)

CLASSWISE PRECISION

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/NAIVE%20BAYES/641cc186-9fa1-44ed-b623-67893a86df66.png?raw=true)

CLASSWISE RECALL

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/NAIVE%20BAYES/24737c59-c851-4acc-b2b3-12436330c5a0.png?raw=true)

CLASSWISE F1_SCORE

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/NAIVE%20BAYES/d9c2e397-4a34-4569-9296-6fdcd25964d5.png?raw=true)

# DECISION TREE

## ACCURACY: 44.6875%

### CONFUSION MATRIX:

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/DECISION%20TREE/1962b6be-ccd9-4d77-a7f7-9e813dcd61d7.png?raw=true)

CLASSWISE ACCURACY:

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/DECISION%20TREE/d9414024-6204-4cff-9005-9c31e99d9c33.png?raw=true)

CLASSWISE PRECISION:

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/DECISION%20TREE/c9b2592f-079d-46e6-8d4d-97b3942b8817.png?raw=true)

CLASSWISE RECALL

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/DECISION%20TREE/bdadfd4a-0751-4cb4-8b07-9070ca563bcd.png?raw=true)

CLASSWISE F1_SCORE

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/DECISION%20TREE/c50bb305-5b6b-4f9c-aab3-3fd4202f02e7.png?raw=true)

### INSIGHTS FROM THE GRAPHS :

1. DUE TO CLASS IMBALANCE, THERE IS THERE IS NOT MUCH CHANGE IN THE METRIC EVALUATION OF CLASSES EXCEPT 5 AND 6 WHICH ARE THE MOST DENSIFIED CLASSES IN THE DATASET. SO SLIGHT CHANGE IN THE PREDICTION OF THESE IMPACTS THE ACCURACY OF THE MODEL.

2. DECISION TREE PREDICTIONS ARE SIMILAR TO NAIVE BAYES EXCEPT IT GIVES MORE ACCURACY FOR 5 THAN THE FORMER MODEL.

# ARTIFICIAL NEURAL NETWORKS FROM SCRATCH AND WITH TENSORFLOW AND KERAS:

## ACCURACY: 54.06% AFTER 100 EPOCHS OF TRAINING.

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/ANN/Screenshot%202023-07-15%20102149.png)

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/ANN/Screenshot%202023-07-15%20102238.png)

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/ANN/Screenshot%202023-07-15%20102320.png)

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/ANN/Screenshot%202023-07-15%20102350.png)

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/ANN/Screenshot%202023-07-15%20102445.png)

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/ANN/Screenshot%202023-07-15%20102516.png)

![](https://github.com/PARANTAPMISHRA/DATABYTE_INDUCTION_TASKS/blob/main/DATABYTE%20TASK%20IMAGES/ANN/Screenshot%202023-07-15%20102552.png)

# CONCLUSION:

1. OUT OF ALL THE MODELS IMPLEMENTED NAIVE BAYES GIVE THE MAXIMUM ACCURACY. THIS CAN BE DUE TO THE FOLLOWING PARAMETER:

1. OUTLIERS: AS NAIVE BAYES ASSUMES VERY LESS CORRELATION BETWEEN THE FEATURES THUS EFFECT OF OUTLIERS IS VERY LESS.

1. CLASSIMBALANCE: THE EFFECT OF CLASSIMBALANCE IS LESS AS IT OPERATES ON THE PRINCIPLE OF PROBABILITY DISTRIBUTION.

1. Also, ANN AND DECISION TREE ARE MUCH MORE COMPLEX ALGORITHMS AS COMPARED TO NAIVE BAYES. THUS THERE IS A CHANCE THAT THESE MODELS MAY REQUIRE MORE DATASETS THAN PROVIDED WHICH IS JUST 1599 DATAPOINT WITH 11% OUTLIERS AND A LARGE AMOUNT OF CLASS IMBALANCE.

# 1. ALSO I TRIED TO REMOVE THE CLASS IMBALANCE BY USING LIBRARIES, THEN TRIED TO IMPLEMENT THE ANN. RESULTS WERE AS FOLLOWS:
     
      1. MODEL PERFORMED WELL ON THE TRAINING DATA WITH ACCURACY OF 50% IN 4 EPOCHS AND 
        ACCURACY OF 95.48% AT 500 EPOCHS.
      1. BUT WHEN EVALUATED ON THE TEST DATASET ACCURACY DROPED DOWN TO 47.81%.
      1. THUS ITS A CLEAR EXAMPLE OF OVERFITTING OF THE ANN ON SUCH A SMALL DATASET.
   
