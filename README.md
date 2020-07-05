# Shopee Code League 2020 - Product Detection 

This is source code for 4th place (Private LB: 0.84923) of [[Student] Shopee Code League 2020 - Product Detection](https://www.kaggle.com/c/shopee-product-detection-student). Check [Overview Archive](https://archive.is/EqTMR) and [Leaderboard Archive](https://archive.is/wrXZa) if Kaggle is down or the link is invalid.

## Warning

* There's no reproducibility guarantee for notebook which uses GPU and TPU
* Although we use License "The Unlicense", dataset and generated dataset falls under Shopee Terms and Conditions which can be seen on [Google Docs](https://docs.google.com/document/d/17mWGXdK8kW9wMxiAPWrn_1MnDtCRKxRdiSoz1u5RRDw), [Google Docs (2)](https://docs.google.com/document/d/13-ZxPKqHL0o5CG8YJSHjNe_cJUQnxjctCBRfu_S3sVc/) or [Internet Archive](https://web.archive.org/web/20200704093857/https://docs.google.com/document/d/17mWGXdK8kW9wMxiAPWrn_1MnDtCRKxRdiSoz1u5RRDw/edit)

## Environment List

> Some of the notebook are run on different environment

| Environment Name | Description                            |
| ---------------- | -------------------------------------- |
| Kaggle CPU       | 2C/4T CPU, 16GB RAM                    |
| Kaggle GPU       | 2C/4T CPU, 16GB RAM, Nvidia Tesla P100 |
| Kaggle TPU       | 2C/4T CPU, 16GB RAM, TPU v3-8          |
| Local            | 6C/12T CPU, 16GB RAM, 16GB Swapfile    |

To ensure you can run jupyter notebook which runs on "Local" environment, make sure that :

1. Use OS based on GNU/Linux
2. Use Python 3.8
3. Install required application & library

```
sudo apt update
sudo apt install enchant libenchant hunspell libhunspell hunspell-en-us hunspell-id
```

4. Install required Python library

```
python3.8 -m pip install pandas matplotlib seaborn nltk pyenchant jellyfish scikit-learn scipy numpy pattern notebook
```

## Notebook description

> Jupyter notebook on `extra_notebook` directory isn't used on the competition

| Filename           | Link to Kaggle Kernel                                                                      | Environment | Description                                                                                             |
| ------------------ | ------------------------------------------------------------------------------------------ | ----------- | ------------------------------------------------------------------------------------------------------- |
| 01a_ocr.ipynb      | https://www.kaggle.com/ilosvigil/shopee-competition-2-ocr?scriptVersionId=37547674         | Kaggle GPU  | Perform OCR on Train Images (0 - 26346)                                                                 |
| 01b_ocr.ipynb      | https://www.kaggle.com/ilosvigil/shopee-competition-2-ocr?scriptVersionId=37573844         | Kaggle GPU  | Perform OCR on Train Images (26347 - 52691)                                                             |
| 01c_ocr.ipynb      | https://www.kaggle.com/ilosvigil/shopee-competition-2-ocr?scriptVersionId=37601445         | Kaggle GPU  | Perform OCR on Train Images (52695 - 79041)                                                             |
| 01d_ocr.ipynb      | https://www.kaggle.com/williammulianto/shopee-2-ocr-train-41b3f4?scriptVersionId=37614455  | Kaggle GPU  | Perform OCR on Train Images (79042 - 105390)                                                            |
| 01e_ocr.ipynb      | https://www.kaggle.com/ilosvigil/shopee-competition-2-ocr?scriptVersionId=37631409         | Kaggle GPU  | Perform OCR on Test Images                                                                              |
| 02a_clean.ipynb    | -                                                                                          | Local       | Clean OCR text from train images                                                                        |
| 02b_clean.ipynb    | -                                                                                          | Local       | Clean OCR text from text images                                                                         |
| 03_tfidf.ipynb     | -                                                                                          | Local       | Create TF-IDF representation of cleaned text. **Warning:** use lots of RAM when creating parquest file. |
| 04a_tfrecord.ipynb | https://www.kaggle.com/ilosvigil/scl2020-2-4a-create-tfrecord-1-3?scriptVersionId=37853684 | Kaggle CPU  | Create TFRecord file from train images & parquet dataset (0 - 52694)                                    |
| 04b_tfrecord.ipynb | https://www.kaggle.com/ilosvigil/scl2020-2-4b-create-tfrecord-2-3?scriptVersionId=37853702 | Kaggle CPU  | Create TFRecord file from train images & parquet dataset (52695 - 105390)                               |
| 04c_tfrecord.ipynb | https://www.kaggle.com/ilosvigil/scl2020-2-4c-create-tfrecord-3-3?scriptVersionId=37853715 | Kaggle CPU  | Create TFRecord file from test images & parquet dataset                                                 |
| 05a_model.ipynb    | https://www.kaggle.com/ilosvigil/scl2020-2-5-model?scriptVersionId=37953296                | Kaggle TPU  | Create Multimodal Model. Some comment might not match code.                                             |
| 05b_model.ipynb    | https://www.kaggle.com/ilosvigil/shopee-competition-2?scriptVersionId=38054791             | Kaggle TPU  | Create Multimodal Model                                                                                 |

## Generated Dataset

Generated dataset from jupyter notebook is available on this repository and/or Kaggle datasets platform.

| Notebook Filename  | Directory path                | Link to Kaggle datasets                                    |
| ------------------ | ----------------------------- | ---------------------------------------------------------- |
| 01a_ocr.ipynb      | `dataset/1_ocr_text`          | https://www.kaggle.com/ilosvigil/sc-21-ocr                 |
| 01b_ocr.ipynb      | `dataset/1_ocr_text`          | https://www.kaggle.com/ilosvigil/sc-21-ocr                 |
| 01c_ocr.ipynb      | `dataset/1_ocr_text`          | https://www.kaggle.com/ilosvigil/sc-21-ocr                 |
| 01d_ocr.ipynb      | `dataset/1_ocr_text`          | https://www.kaggle.com/ilosvigil/sc-21-ocr                 |
| 01e_ocr.ipynb      | `dataset/1_ocr_text`          | https://www.kaggle.com/ilosvigil/sc-21-ocr                 |
| 02a_clean.ipynb    | `dataset/2_with_cleaned_text` | -                                                          |
| 02b_clean.ipynb    | `dataset/2_with_cleaned_text` | -                                                          |
| 03_tfidf.ipynb     | `dataset/3_with_tfidf`        | https://www.kaggle.com/ilosvigil/csv-with-cleaned-ocr-text |
| 04a_tfrecord.ipynb | -                             | https://www.kaggle.com/ilosvigil/tfrecords                 |
| 04b_tfrecord.ipynb | -                             | https://www.kaggle.com/ilosvigil/tfrecords-2               |
| 04c_tfrecord.ipynb | -                             | https://www.kaggle.com/ilosvigil/tfrecords-3               |

## LB/Leaderboard Score

| Notebook filename | Submission filename    | Used for Final Score | Public LB   | Private LB  |
| ----------------- | ---------------------- | -------------------- | ----------- | ----------- |
| 05a_model.ipynb   | submission.csv         | Yes                  | **0.85325** | **0.84923** |
| 05b_model.ipynb   | submission.csv         | No                   | 0.84085     | 0.84339     |
| 05b_model.ipynb   | submission_tta_0.csv   | Yes                  | 0.84323     | 0.84244     |
| 05b_model.ipynb   | submission_tta_all.csv | No                   | 0.84085     | 0.84339     |

## Reproducibility Guide

> This guide assume you have necessary files (full dataset provided by Shopee) and move it to correct directory path

1. Run `01a_ocr.ipynb`, `01b_ocr.ipynb`, `01c_ocr.ipynb`, `01d_ocr.ipynb` & `01e_ocr.ipynb` on Kaggle Notebook
2. Rename output filename from each notebook

| Notebook Filename | Old filename | New Filename    |
| ----------------- | ------------ | --------------- |
| 01a_ocr.ipynb     | train2a.csv  | train_ocr_1.csv |
| 01b_ocr.ipynb     | train2a.csv  | train_ocr_2.csv |
| 01c_ocr.ipynb     | train2c.csv  | train_ocr_3.csv |
| 01d_ocr.ipynb     | train2d.csv  | train_ocr_4.csv |
| 01e_ocr.ipynb     | test2.csv    | test_ocr.csv    |

3. Run `02a_clean.ipynb` & `02b_clean.ipynb`
4. Run `03_tfidf.ipynb`
5. Run `04a_tfrecord.ipynb`, `04b_tfrecord.ipynb` & `04c_tfrecord.ipynb`
6. Run `05a_model.ipynb` or `05b_model.ipynb`
