# ml


5:
1. Mean vs median imputation: The mean is affected by outliers. The median is robust. With extreme
outliers in Age, use the median.
2. Why train/test split: To evaluate the model on unseen data and detect overfitting.
3. Label vs one-hot encoding: Label encoding assigns integers (0, 1, 2) and implies an order, so it suits
ordinal data. One-hot makes a binary column per category and suits nominal data.
4. Outliers: Data points far from most others. A histogram shows the distribution shape. A boxplot
shows the median, quartiles, and outliers.
5. Feature scaling: Puts features on a similar range so that large-valued features do not dominate
(important for KNN, SVM, gradient descent, PCA).
6. Effect of missing values: They cause errors, bias, and reduced accuracy, and many algorithms cannot
handle them.
7. Why preprocessing is necessary: Real data is noisy, incomplete, and inconsistent. Clean data gives
better models


6:
1. Regression vs classification: Regression predicts a continuous value (price). Classification predicts a
discrete class (spam / not spam).
2. Features vs target: Features are the input variables (X). The target is the output to predict (y).
3. How linear regression models the relationship: It fits y = w1x1 + w2x2 + ... + b by minimizing
squared error.
4. MSE: Mean of squared errors. It penalizes large errors heavily.
5. MAE: Mean of absolute errors. It is easy to interpret and less sensitive to outliers.
6. R² score: Proportion of variance in the target explained by the model. 1 is perfect, 0 is no better than
predicting the mean.


7:
1. K too small / too large (KNN): Too small (k=1) gives overfitting and sensitivity to noise. Too large
gives underfitting and blurred class boundaries. Choose k by cross-validation (usually odd).
2. Why scaling matters for KNN: KNN uses distances, so large-range features would dominate.
3. Accuracy on imbalanced data: A model that always predicts the majority class gets high accuracy
but is useless. Use precision, recall, F1-score, ROC-AUC.
4. Classification vs regression: Classification predicts categories, regression predicts continuous values.
5. Why logistic regression is used for classification: It passes a linear combination through the
sigmoid function to output a probability between 0 and 1, then thresholds it (usually 0.5).
6. How it estimates probability: P(y=1) = 1 / (1 + e^-(w·x + b)).
7. Confusion matrix: Shows TP, TN, FP, FN, from which accuracy, precision, recall, and F1 are computed.


8:
1. Entropy: A measure of impurity or uncertainty in a node. Entropy = -Σ p·log2(p). It is 0 for a pure node.
2. Information gain: Entropy(parent) minus the weighted entropy of the children. The tree splits on the
feature with the highest gain.
3. Role of entropy in the tree: It decides which feature gives the best split at each node.
4. Decision tree vs Naïve Bayes: A tree is rule-based, interpretable, and can overfit. Naïve Bayes is
probabilistic, assumes features are independent, is fast, and works with small data.
5. Why Naïve Bayes is probabilistic: It uses Bayes' theorem to compute P(class | features) and picks
the class with the highest posterior probability.
6. Label vs one-hot encoding: Label gives integer codes (ordinal). One-hot gives a binary column per
category (nominal).


9:
 Supervised vs unsupervised: Supervised learns from labeled data. Unsupervised finds patterns in
unlabeled data.
2. Clustering vs classification: Clustering is unsupervised and groups unlabeled data. Classification is
supervised and assigns known labels.
3. How K-Means works: Pick k centroids, assign each point to the nearest centroid, recompute centroids
as cluster means, and repeat until stable.
4. Elbow method: Plot WCSS (inertia) against k. The best k is at the "elbow", where the drop in WCSS
flattens.
5. Why the number of clusters matters: Too few merges distinct groups. Too many splits natural
groups and overfits.
6. Dendrogram: A tree diagram showing how clusters merge (or split). Cutting it at a chosen height gives
the number of clusters (the largest vertical gap without merges suggests where to cut).
7. K-Means vs hierarchical: K-Means needs k in advance, is fast, and gives flat clusters. Hierarchical
needs no k, builds a tree, and is slower on big data.


10:
1. Dimensionality reduction: Reducing the number of features while keeping most of the information. It
reduces computation, noise, and overfitting, and allows visualization.
2. Why standardize before PCA: PCA picks directions of maximum variance, so features with large
scales would dominate. Standardizing gives each feature equal weight.
3. What PCA does: It finds orthogonal principal components (eigenvectors of the covariance matrix)
ordered by the variance they explain.


11:
1. Bagging vs boosting: Bagging (Random Forest) trains trees in parallel on random bootstrap samples
and averages or votes, which reduces variance. Boosting (AdaBoost) trains weak learners sequentially,
each focusing on previous errors, which reduces bias.
2. Why cross-validation: It gives a more reliable estimate of performance, uses all the data for training
and testing, and reduces overfitting to one split.
3. Purpose of feature scaling: Puts features on a comparable scale. It is essential for distance- or
margin-based models (SVM, KNN) and gradient descent.
4. Grid search: Tries every combination of the given hyperparameters with cross-validation and returns
the best one.
5. SVM: Finds the hyperplane that maximizes the margin between classes. Kernels (RBF) handle non-linear
data.

