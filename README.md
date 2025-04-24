# Road Traffic Accident Analysis Using Machine Learning and Neural Networks

## Overview

Road Traffic Accidents (RTAs) are a major public health concern globally and are particularly prevalent in developing countries such as Pakistan. In these regions, inadequate road infrastructure and weak traffic management systems exacerbate the issue. Unfortunately, RTA data is often underreported or ignored, limiting effective intervention and prevention strategies.

This project presents a data-driven approach to analyzing RTA data from **Rawalpindi, Punjab**, using various machine learning models and a custom-built neural network. The goal is to uncover patterns in **injury types** and **patient status** to help inform future public safety policies.

---

## Objectives

- Analyze road traffic accident data to identify trends and risk factors.
- Predict:
  - **Patient status** (e.g., deceased, injured, uninjured)
  - **Type of injury** sustained
- Compare the performance of different machine learning models, including a custom neural network.

---

## Best Models

| Model             | Patient Status (Accuracy / F1 Score) | Injury Type (Accuracy / F1 Score) |
|------------------|--------------------------------------|-----------------------------------|
| XGBoost          | 0.7299 / 0.7268                      | 0.7598 / 0.7061                   |
| Multi-class ANN  | 0.7197 / 0.7170                      | 0.7690 / 0.6992                   |

Our results indicate that **XGBoost** and the **Multi-class Artificial Neural Network (ANN)** consistently outperformed other models, making them well-suited for RTA analysis.

---

## Key Findings

- Identified high-risk factors contributing to severe RTAs.
- Machine learning methods offer promising accuracy for classifying patient outcomes and injury types.
- Potential to improve emergency response strategies and public policy formulation.

---

---

## Difficulties and Workaround

One of the primary challenges of this study was dealing with the dataset [[2]](#2), which exhibited significant **class imbalance** across both target variables: **Injury Type** and **Patient Status**. As shown in Figures 1 and 2 and Tables 1 and 2 (not included here), certain classes were **overrepresented** while others were **underrepresented**. For example, the number of "Alive" patients greatly exceeded those classified as "Dead", leading to skewed class distribution.

This imbalance posed a risk of biased model performance, particularly underperforming on minority classes. To mitigate this, we:

- Used **stratified data splits** to maintain class proportions.
- Paid special attention to retaining underrepresented classes during preprocessing.

Despite the imbalance, our models demonstrated **strong performance metrics** (accuracy, precision, recall, and F1 score), validating our mitigation strategies.

---

## Future Work

We plan to:

- **Extend the dataset** with samples from other regions and countries to enhance generalization.
- **Develop real-time predictive models** for deployment in accident-prone areas.
- Improve **hospital readiness** by integrating predictive systems into emergency response workflows.

This can potentially reduce casualties by enabling proactive measures and optimizing emergency services for incoming accident cases.

---

## Conclusion

This study offers a comprehensive analysis of road traffic accidents in Rawalpindi, Pakistan, using both traditional machine learning models and custom neural networks.

Despite challenges with **imbalanced data**, our preprocessing pipeline — including tokenization, vectorization, hyperparameter tuning, and stratified sampling — enabled our models to achieve over **70% accuracy** in most tasks.

While the results are promising, **ongoing improvements in model design and data handling** are essential to further enhance predictive power and practical utility in traffic safety analytics.

---

## References

1. U. Farooq, J. Bhatti, M. Siddiq, et al., “Road traffic injuries in Rawalpindi city, Pakistan,” *Eastern Mediterranean Health Journal*, vol. 17, pp. 647–653, Sep. 2011. DOI: [10.26719/2011.17.9.647](https://doi.org/10.26719/2011.17.9.647)

2. M. S. Abid, *Road traffic accident dataset, Rawalpindi-Punjab, Pakistan*. Chishti, Shujaat, 2024. DOI: [10.7910/DVN/4VGTDR](https://doi.org/10.7910/DVN/4VGTDR)

3. T. Mikolov, K. Chen, G. Corrado, and J. Dean, "Efficient Estimation of Word Representations in Vector Space", 2013. [arXiv:1301.3781](https://arxiv.org/abs/1301.3781)

4. R. Řehůřek and P. Sojka, "Software Framework for Topic Modelling with Large Corpora", *LREC 2010 Workshop*, pp. 45–50.

5. F. Pedregosa et al., "Scikit-learn: Machine Learning in Python", *Journal of Machine Learning Research*, vol. 12, pp. 2825–2830, 2011.

6. K. Fukushima, "Visual Feature Extraction by a Multi-layered Network of Analog Threshold Elements", *IEEE Transactions on Systems Science and Cybernetics*, vol. 5, no. 4, pp. 322–333, 1969. DOI: [10.1109/TSSC.1969.300225](https://doi.org/10.1109/TSSC.1969.300225)

7. N. Srivastava et al., "Dropout: A Simple Way to Prevent Neural Networks from Overfitting", *Journal of Machine Learning Research*, vol. 15, no. 1, pp. 1929–1958, Jan. 2014.

---


