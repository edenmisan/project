## Traffic Crashes Injury Prediction

## Dataset Usage Note

Due to its large size, the full dataset cannot be loaded directly from GitHub during execution.
Therefore, the dataset must be downloaded manually from this repository before running the notebook.

When downloaded from GitHub, the file may be saved with a .txt extension.
This file is still a standard CSV-formatted dataset and should be read accordingly.

After downloading the file and placing it in the project directory, the notebook can be executed normally

## Project Overview

This project investigates traffic crash data from the Chicago Data Portal using both supervised and unsupervised machine learning approaches.

The supervised task focuses on predicting whether a traffic crash results in an injury, with emphasis on recall due to the safety-critical nature of the problem.
In parallel, an unsupervised clustering analysis is conducted to explore latent crash patterns without relying on injury labels, providing complementary insight into crash characteristics.

## Dataset

Source: Chicago Data Portal – Traffic Crashes – Crashes

Unit of analysis: Individual traffic crashes

Target variable (supervised task):

INJURY = 1 → injury involved

INJURY = 0 → no injury

Class imbalance: ~79% non-injury vs. ~21% injury crashes

## Supervised Learning: Injury Prediction
### Models

Logistic Regression

Random Forest

Gradient Boosting

Support Vector Machine (SVM)

k-Nearest Neighbors (KNN)

### Domain-Specific Techniques

Handling class imbalance using class weighting

F2-score–oriented evaluation to prioritize recall

Feature selection based on Random Forest feature importance

Feature importance thresholding (importance > 0.005) to reduce noise and dimensionality

## Unsupervised Learning: Crash Pattern Discovery

To complement the supervised classification task, unsupervised clustering was applied to identify latent structures in the crash data without using the injury label.

### Clustering Approach

Algorithm: KMeans

Feature space: Environmental, temporal, and infrastructural crash features

Dimensionality reduction: PCA for visualization

### Cluster Evaluation

Number of clusters selected using:

Elbow method

Silhouette score

Davies–Bouldin index

### Key Insights

Clusters were primarily differentiated by temporal crash patterns

Despite not using injury labels, clusters exhibited different injury rates

This indicates that the clustering captured meaningful risk-related structures in the data

### Evaluation Metrics

Primary metric (supervised): F2-score

Additional metrics: Recall, Precision, ROC-AUC, PR-AUC

Clustering quality metrics: Silhouette score, Davies–Bouldin index

## Project Structure
├── project.ipynb                     # Main notebook: preprocessing, supervised models, clustering, and evaluation
├── Traffic_Crashes_-_Crashes.csv     # Raw traffic crashes dataset (managed with Git LFS)
├── Project_Final_WriteUp.docx        # Final project report (written submission)
├── requirements.txt                  # Python dependencies
├── .gitignore                        # Git ignore configuration
├── .gitattributes                    # Git LFS configuration
├── README.md                         # Project documentation


## Results Summary

Ensemble models achieved the strongest recall-oriented performance in injury prediction

Feature selection improved interpretability and efficiency

Clustering revealed latent temporal crash patterns and meaningful differences in injury risk

## Team Members
- Eden Misan  
- Hadar Yakir
