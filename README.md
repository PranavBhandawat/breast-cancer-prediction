# breast-cancer-prediction
## 📊 Results Summary

This project involved evaluating multiple machine learning classifiers on the breast cancer dataset across different experimental setups:

- **Set 1 (Raw Data):**  
  - Random Forest, XGBoost, and SVM consistently achieved high accuracy (often above 95%).  
  - Naive Bayes variants (GaussianNB, BernoulliNB, MultinomialNB) performed noticeably worse.

- **Set 2 (SMOTE Oversampling):**  
  - Oversampling the minority class significantly improved results for most classifiers.  
  - Random Forest accuracy jumped from ~98% to ~99%.  
  - SVM improved from 93% to 96%.  
  - Naive Bayes showed marginal or negative gains; GaussianNB and BernoulliNB actually dropped in accuracy due to oversampling.

- **Set 3 (Top 15 Feature Selection):**  
  - Tree-based models retained high accuracy with little to no performance loss.  
  - XGBoost and Random Forest remained highly effective.

- **Set 4 (PCA with n = 3):**  
  - PCA helped Naive Bayes models and SVM significantly, improving their accuracy.  
  - This dimensionality reduction was particularly beneficial for models that assume feature independence.

- **Set 5 & 6 (PCA with 10–15 Components):**  
  - Moderate PCA still preserved most classifier performance.  
  - XGBoost and SVM remained the top performers even with fewer features.  
  - Naive Bayes models improved relatively but continued to underperform compared to tree-based models.

### 🏆 Final Verdict:
- **Best Model:** XGBoost with SMOTE (Set 2 & 3) **~99% Accuracy**   
- Followed closely by Random Forest (**~99%**) and SVM (**~97%**)  
- **Naive Bayes:** Worked better with PCA but lagged overall (GaussianNB and BernoulliNB peaked at ~94% in Set 1)
