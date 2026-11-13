# Product Review Analytics Using Hadoop MapReduce and Machine Learning

## Project Overview
This project analyzes Amazon Electronics customer reviews using Apache Hadoop MapReduce and Machine Learning.

It combines large-scale product review analytics with sentiment classification using Logistic Regression.

## Dataset Details
- Dataset: Amazon Reviews 2023 - Electronics
- Platform: Hugging Face
- URL: https://huggingface.co/datasets/McAuley-Lab/Amazon-Reviews-2023
- Total Reviews: 43,886,944
- Unique Products: 1,946,161

## Technologies Used
- Python 3.14.1
- Apache Hadoop 3.3.6
- Hadoop MapReduce
- HDFS
- Hadoop Streaming
- Scikit-learn
- TF-IDF
- Logistic Regression
- Ubuntu Linux

## Project Modules

### 1. Big Data Analytics
- Custom Python Mapper and Reducer.
- Processed Amazon reviews using Hadoop Streaming.
- Calculated product-wise review counts.
- Calculated average product ratings.
- Generated 1-star to 5-star rating distributions.
- Identified most-reviewed and highest-rated products.

### 2. Sentiment Analysis
- Feature extraction using TF-IDF.
- Classification using Logistic Regression.
- 1–2 star reviews labelled Negative.
- 4–5 star reviews labelled Positive.
- 3-star reviews excluded.

The initial ML experiment used 15,600 balanced reviews sampled from the first Parquet file.

## Machine Learning Results

| Metric | Score |
|---|---:|
| Accuracy | 86.54% |
| Precision | 87.80% |
| Recall | 84.87% |
| F1 Score | 86.31% |

Training samples: 12,480  
Testing samples: 3,120

## Hadoop Results

| Metric | Result |
|---|---:|
| Total Input Reviews | 43,886,944 |
| Valid Reviews | 43,886,942 |
| Excluded Reviews | 2 |
| Unique Products | 1,946,161 |
| Overall Average Rating | 4.09923 |

## Project Structure

```text
product_review_analytics/
├── mapreduce/
│   ├── mapper.py
│   ├── reducer.py
│   └── sample.txt
├── ml/
│   ├── inspect_dataset.py
│   ├── prepare_data.py
│   ├── train_model.py
│   └── logistic_regression_model.pkl
├── results/
│   └── project_summary.txt
├── .gitignore
└── README.md
