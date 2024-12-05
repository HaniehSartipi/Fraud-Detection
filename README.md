# Fraud-Detection
Exploratory Data Analysis (EDA)

Checked for missing values (none found) and duplicates (none found).
Visualized the amount feature with a histogram, observing most values are low.
Used bar charts for categorical features, e.g., most common source_prefix and dest_prefix values are "Whiskers"; most frequent agent is "A".
Scatter plots showed most fraud (label=1) transactions occur with low amounts.

Supervised Learning: Random Forest

Feature Engineering: Dropped features like amount, label, and others to improve model performance.
Handled class imbalance (fraud vs. non-fraud) using SMOTE for oversampling.
Skipped feature scaling as Random Forest doesn’t require it.
Evaluated model with confusion matrix, accuracy, precision, and recall.
Performed backward selection to identify important features.
Best model excluded ['label','source_postfix','source_prefix','agent','amount'].

Unsupervised Learning: KMeans and GMM with PCA

Used PCA for dimensionality reduction, selecting 2 components via elbow plot for better clustering.
Determined 3 optimal clusters via elbow plot; evaluated with silhouette scores.
Best clustering achieved using only amount and status features.
PCA improved clustering performance and visualization by reducing dimensions and removing feature correlation.
