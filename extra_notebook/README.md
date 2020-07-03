# Extra Notebook

Jupyter Notebook on this directory isn't used on the competition

| Filename                               | Description                                                           |
| -------------------------------------- | --------------------------------------------------------------------- |
| 01_analyze_train_image.ipynb           | EDA on train images                                                   |
| 02_analyze_test_image.ipynb            | EDA on test images                                                    |
| 03_classification_text.ipynb           | Product Classification with Bag of Words & TD-IDF word representation |
| 04_classification_embedding_text.ipynb | Product Classification with Bag of Words & TD-IDF word representation |

## Score

| Filename                               | Model name | Desc                                                 | Public score | Private score |
| -------------------------------------- | ---------- | ---------------------------------------------------- | ------------ | ------------- |
| 03_classification_text.ipynb           | model1     | BoW + NN                                             | 0.28714      | ?             |
| 03_classification_text.ipynb           | model2     | BoW + MLP                                            | 0.28477      | ?             |
| -                                      | -          | TF-IDF + NN                                          | 0.27949      | ?             |
| 03_classification_text.ipynb           | model3     | TF-IDF + MLP                                         | 0.29031      | ?             |
| 04_classification_embedding_text.ipynb | model1     | FastText + Bi-LSTM + Many to One Attention Mechanism | 0.25283      | ?             |
| 04_classification_embedding_text.ipynb | model1     | FastText + Bi-LSTM                                   | -            | -             |
