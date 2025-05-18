 Evaluating-classification-models
 Given the MAGIC gamma telescope dataset that can be obtained using this Link. This dataset 
 is generated to simulate registration of high energy gamma particles in a ground-based atmo- 
 spheric Cherenkov gamma telescope using the imaging technique. The dataset consists of two 
 classes; gammas (signal) and hadrons (background). There are 12332 gamma events and 6688 
 hadron events. You are required to use this dataset to apply different classification models 
 such as Decision Trees, N a¨ı ve Bayes Classifier, Random   Forests and AdaBoost You are 
 also required to tune the parameters of these models, and compare the performance of 
 models with each other. 


 ✅ **Objectives of the Code**

This Python code is designed to perform a complete **classification analysis** on the **MAGIC Gamma Telescope dataset**. The main objectives are:

1. **Load and explore the dataset** to understand its structure and class distribution.
2. **Balance the dataset** to avoid bias due to class imbalance.
3. **Split the data** into training and testing sets.
4. **Train and optimize multiple classification models**, including:

   * Decision Tree
   * AdaBoost
   * Random Forest
   * Naive Bayes
5. **Evaluate the models** using standard performance metrics:

   * Accuracy
   * Precision
   * Recall
   * F1-score
   * Confusion matrix
   * ROC curve and AUC
6. **Compare models** based on their performance.
7. **Visualize results** such as:

   * Class distribution
   * Feature importance
   * Decision tree structure
   * Confusion matrices and ROC curves
8. **Save the results** to a CSV file for further analysis.

---

### 📊 **Output and Results Summary**

#### 1. **Dataset Shape and Class Distribution**

* Original dataset shape: `(19020, 11)`
* Imbalanced class distribution:

  ```
  g (gamma)     ≈ 12332
  h (hadron)    ≈ 6688
  ```
* After balancing: equal samples from both classes (\~6688 each).

**Importance:** Balancing prevents the models from being biased toward the majority class (gamma).

---

#### 2. **Trained Models and Tuning**

Each model was trained using hyperparameter tuning (GridSearchCV) except Naive Bayes.

* **Decision Tree**:

  * Visualized the tree structure.
  * Tuned using depth and min samples split.
* **AdaBoost**:

  * Feature importance plotted.
  * Tuned using `n_estimators` and `learning_rate`.
* **Random Forest**:

  * Feature importance plotted.
  * Tuned using `n_estimators`, `max_depth`, and `min_samples_split`.
* **Naive Bayes**:

  * No tuning, used as a baseline.

---

#### 3. **Model Evaluation Metrics**

Each model was evaluated using:

* **Accuracy**: Overall correct predictions.
* **Precision**: True positives / (True positives + False positives).
* **Recall**: True positives / (True positives + False negatives).
* **F1 Score**: Harmonic mean of precision and recall.
* **ROC AUC**: Area under the ROC curve.
* **Confusion Matrix**: Visual representation of prediction errors.

**Importance:** These metrics help us understand not just how many predictions are correct, but *how* they are correct, especially in binary classification.

---

#### 4. **Visual Outputs**

* **class\_distribution.png**: Original and balanced class visualization.
* **decision\_tree.png**: Structure of the trained decision tree.
* **feature\_importance** (for AdaBoost & Random Forest): Helps identify the most influential features.
* **confusion\_matrix\_\*.png**: For each model.
* **roc\_curve\_\*.png**: For each model with AUC score.
* **model\_comparison.png**: Bar chart comparing Accuracy, Precision, Recall, F1-score.

---

#### 5. **Final Result File**

* `model_results.csv`: Contains performance metrics for all models in tabular format.

