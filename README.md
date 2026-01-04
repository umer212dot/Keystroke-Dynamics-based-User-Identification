# Keystroke-Dynamics-based-User-Identification
This project presents a keystroke dynamics–based user authentication system that utilizes behavioral biometrics to identify users based on their typing patterns. A web-based application was developed to collect keystroke data from 17 users, generating a dataset of 1,020 samples (60 samples per user). From raw keystroke logs, a total of 12 timing- and behavior-based features were selected for model training, capturing individual typing characteristics such as inter-key delays, hold times, error patterns, and typing rhythm.

The complete dataset contained the following collected attributes:
userID, autocorrLag1IKD, avgBurstLength, avgHoldTime, avgIKD, avgPauseLength, backspaceCount, backspaceRatio, burstCount, commonDigraphTiming, correctionLatencyMean, entropyIKD, errorRate, holdTimeStdDev, ikdStdDev, maxBurstLength, medianIKD, pauseCount, shiftPressCount, skewnessIKD, tempoChangeRate, typingSpeedWPM,
from which 12 relevant features were selected for training after preprocessing.

Exploratory Data Analysis (EDA) and preprocessing were performed to improve data quality. Feature selection techniques, including ANOVA and Random Forest feature importance, were applied to identify discriminative attributes. Principal Component Analysis (PCA) was used for variance analysis and interpretability, where the first five principal components explained approximately 81% of the total variance.

Multiple machine learning models were trained and evaluated using an 80/20 train-test split per user, including K-Nearest Neighbors, Logistic Regression, Support Vector Machines, Decision Trees, Random Forests, Naive Bayes, AdaBoost, Gradient Boosting, Multilayer Perceptron (MLP), and Perceptron. The MLP classifier achieved the highest accuracy of 80%, outperforming both classical and ensemble models.

# Results Summary
| Model               | Accuracy |
| ------------------- | -------- |
| MLP                 | 80.00%   |
| Random Forest       | 77.06%   |
| Logistic Regression | 77.06%   |
| Naive Bayes         | 75.29%   |
| Decision Tree       | 72.94%   |
| Custom KNN          | 72.35%   |
| SVM                 | 72.35%   |
| KNN                 | 71.18%   |
| Gradient Boosting   | 69.41%   |
| Perceptron          | 67.06%   |
| AdaBoost            | 22.35%   |
