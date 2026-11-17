# E-commerce Delivery Status Prediction

CSE422 (Artificial Intelligence) lab project, BRAC University, Summer 2025.

The goal is to predict whether an e-commerce order will be **delivered on time or late**, from shipment and customer details. This is a binary classification problem in the logistics domain.

## Data

The public **E-Commerce Shipping** dataset, with about 11,000 orders. It has 10 input features:
- warehouse block
- mode of shipment
- customer care calls
- customer rating
- cost
- prior purchases
- product importance
- gender
- discount
- weight

The target is the delivery status: on time or late.

The dataset is not included here. Download it and place `E-commerce Shipping Dataset.csv` next to the notebook. The notebook was run on Google Colab, so it reads the file from `/content/`.

## What the notebook does

1. **EDA:** distributions, class balance, and a correlation heatmap.
2. **Preprocessing:** missing-value handling, label and one-hot encoding of categorical features, and standard scaling.
3. **Split:** a stratified 80/20 train/test split, plus 5-fold cross-validation.
4. **Models:** KNN, Decision Tree, Logistic Regression, Naive Bayes, and a Neural Network (MLP), all with scikit-learn. K-Means is included as an unsupervised comparison.
5. **Evaluation:** accuracy, precision, recall, F1, confusion matrices, and ROC/AUC.

## Results

| Model | CV accuracy | Test accuracy |
|---|---|---|
| KNN | 0.64 | 0.63 |
| Decision Tree | 0.64 | 0.65 |
| Logistic Regression | 0.64 | 0.64 |
| Naive Bayes | 0.65 | 0.65 |
| **Neural Network** | 0.64 | **0.67** |

The Neural Network gave the best test accuracy. The features carry only a weak signal for delivery status, so all the models land in a similar range.

## Files

| File | Contents |
|---|---|
| `notebook.ipynb` | Full pipeline with outputs and plots |
| `docs/Project_Report.pdf` | Submitted project report. My teammate's student ID is blacked out. |

## Team

Group 15: Tanzim Hossain Ayon, Shuvo Datta.
