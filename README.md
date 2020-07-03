# Shopee Code League 2020 - Product Detection 

This is source code for 3rd Place (Public Leaderboard) with score 0.85325 of [[Student] Shopee Code League 2020 - Product Detection](https://www.kaggle.com/c/shopee-product-detection-student). Open [Overview Archive](https://archive.is/EqTMR) and [Leaderboard Archive](https://archive.is/fHKAz) if Kaggle is down or the links become invalid.

## Environment List

> Some of the notebook are run on different environment

| Environment Name | Description                            |
| ---------------- | -------------------------------------- |
| Kaggle CPU       | 2C/4T CPU, 16GB RAM                    |
| Kaggle GPU       | 2C/4T CPU, 16GB RAM, Nvidia Tesla P100 |
| Kaggle TPU       | 2C/4T CPU, 16GB RAM, TPU v3-8          |
| Local            | 6C/12T CPU, 16GB RAM, 16GB Swapfile    |

## Notebook description

> Jupyter Notebook on `extra_notebook` directory isn't used on the competition

| Filename           | Kaggle link                                                                               | Environment | Description                                                               |
| ------------------ | ----------------------------------------------------------------------------------------- | ----------- | ------------------------------------------------------------------------- |
| 01a_ocr.ipynb      | https://www.kaggle.com/ilosvigil/shopee-competition-2-ocr?scriptVersionId=37547674        | Kaggle GPU  | Perform OCR on Train Images (0 - 26346)                                   |
| 01b_ocr.ipynb      | https://www.kaggle.com/ilosvigil/shopee-competition-2-ocr?scriptVersionId=37573844        | Kaggle GPU  | Perform OCR on Train Images (26347 - 52691)                               |
| 01c_ocr.ipynb      | https://www.kaggle.com/ilosvigil/shopee-competition-2-ocr?scriptVersionId=37601445        | Kaggle GPU  | Perform OCR on Train Images (52695 - 79041)                               |
| 01d_ocr.ipynb      | https://www.kaggle.com/williammulianto/shopee-2-ocr-train-41b3f4?scriptVersionId=37614455 | Kaggle GPU  | Perform OCR on Train Images (79042 - 105390)                              |
| 01e_ocr.ipynb      | https://www.kaggle.com/ilosvigil/shopee-competition-2-ocr?scriptVersionId=37631409        | Kaggle GPU  | Perform OCR on Test Images                                                |
| 02a_clean.ipynb    | -                                                                                         | Local       | Clean OCR text from train images                                          |
| 02b_clean.ipynb    | -                                                                                         | Local       | Clean OCR text from text images                                           |
| 03_tfidf.ipynb     | -                                                                                         | Local       | Create TF-IDF representation of cleaned text                              |
| 04a_tfrecord.ipynb | https://www.kaggle.com/ilosvigil/scl2020-2-4a-create-tfrecord-1-3                         | Kaggle CPU  | Create TFRecord file from train images & parquet dataset (0 - 52694)      |
| 04b_tfrecord.ipynb | https://www.kaggle.com/ilosvigil/scl2020-2-4c-create-tfrecord-2-3                         | Kaggle CPU  | Create TFRecord file from train images & parquet dataset (52695 - 105390) |
| 04c_tfrecord.ipynb | https://www.kaggle.com/ilosvigil/scl2020-2-4b-create-tfrecord-3-3                         | Kaggle CPU  | Create TFRecord file from test images & parquet dataset                   |

## Reproducibility Guide

> This guide assume you move necessary files to correct directory path

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
