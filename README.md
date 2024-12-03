# Website Fingerprinting Classification

## 🌐 Introduction

This project aims to perform a **Website Fingerprinting Attack** by analyzing packet data. Features are extracted from the packet data, and their importance is calculated to identify the most accurate model for classification.

- Closed-world Experiment: The model is trained using only monitored data.
- Open-world Experiment: The trained model is used to classify website data:
  - Binary Classification: Websites are classified as either monitored or unmonitored.
  - Multi-class Classification: Monitored websites are assigned labels from 0 to 94, while unmonitored websites are assigned the label -1.

## 🖥️ How to Run

### 1. Closed-World Experiment

1. Open any of the following files in respository:

- `feature_selection_NaiveBayes.ipynb`
- `feature_selection_SVM.ipynb`
- `feature_selection_RandomForest.ipynb`

  Each file performs feature extraction and calculates accuracy using the **Naive Bayes**, **SVM**, and **Random Forest** models respectively.

2. In **"1. Data Preprocessing"**, change the path for loading the pickle file to the actual path where the mon_standard.pkl file is located.
3. Follow the notebook's instructions to execute each cell sequentially.
4. Check the accuracy and feature importance results.

<br>

---

😎 From here, the main experiments of this project begin!

### 2. Open-world Experiment : Binary Classification

1. Open the following file in repository:

- `binary_classification.ipynb`

2. In **"1. Data Preprocessing"**, change the path for loading the pickle file to the actual path where the 'mon_standard.pkl' and 'unmon_standard10_3000.pkl' files are located.
3. Follow the notebook's instructions to execute each cell sequentially.
4. Check the results of binary classification.  
   In **"4. Result"**, the results can be interpreted by examining the following:
   - Number of Samples Classified (monitored/unmonitored)
   - Confusion Matrix
   - Feature Importance
   - Counts and Correct Predictions per Class
   - Precision-Recall Curve
   - ROC Curve

### 3. Open-world Experiment : Multi-class Classification

1. Open the following file in repository:

- `multi_class_classification.ipynb`

2. In **"1. Determine confidence using the monitored dataset - 1. Data Preprocessing"**, change the path for loading the pickle file to the actual path where the 'mon_standard.pkl' file is located.
3. In **"2. Multi-class classification on the unmonitored dataset - 1. Data Preprocessing"**, change the path for loading the pickle file to the actual path where the 'unmon_standard10_3000.pkl' file is located.
4. Follow the notebook's instructions to execute each cell sequentially.
5. Check the results of multi-class classification.  
   In **"3. Final Result"**, you can check the following results:
   - A dataframe of monitored data classified with labels ranging from 0 to 94
   - A dataframe of unmonitored data classified with the label -1
   - The count of predicted classes
