# RSNA-Breast-Cancer-Detection

## Introduction

Breast cancer is a significant cause of cancer-related fatalities among women globally. Timely detection of breast cancer is critical for successful treatment and improved survival rates. In recent times, deep learning techniques have emerged as promising tools for detecting breast cancer from medical images, including mammograms.

The RSNA Breast Cancer Detection competition, hosted on Kaggle, serves as an important initiative to foster the development of machine learning models for breast cancer detection. Participants are provided with a dataset of mammogram images, accompanied by labels indicating the presence or absence of breast cancer. The primary challenge is to create deep learning models capable of accurately detecting breast cancer from these mammogram images.

In this report, we embark on an exploration of the RSNA Breast Cancer Detection competition, where we will closely examine the approaches and techniques employed by the top-performing models. Our objective is to gain valuable insights into the best practices for utilizing deep learning methods in breast cancer detection and understand the advancements made in this critical field.

# Medical Imaging

The RSNA Breast Cancer Detection competition focuses on medical imaging, specifically the utilization of mammograms for breast cancer detection. Mammography serves as the current gold standard for breast cancer screening and is recommended by medical experts for women over the age of 50. However, mammography has its limitations, including false positives and false negatives, leading to potential consequences such as unnecessary biopsies and missed diagnoses.

## a. Dataset Descriptions

The dataset provided for Task 1 of the RSNA Breast Cancer Detection competition plays a pivotal role in the competition. It comprises over 54,000 digital mammography images in DICOM format, encompassing both cancerous and non-cancerous cases.

The dataset poses unique challenges to developers due to its size and complexity. With a size exceeding 300 GB, processing and analyzing the dataset demands substantial computational resources. Additionally, the dataset exhibits an imbalance, containing a higher number of non-cancerous cases compared to cancerous cases (see Figure 1). This imbalance presents a significant hurdle for the development of accurate models that can successfully detect cancerous cases while minimizing false positives.

To overcome these challenges, developers must engage in extensive pre-processing of the dataset, which includes tasks such as resizing, balancing, and normalization. The pre-processing stage aims to standardize image dimensions, balance the dataset, and enhance image contrast, ultimately improving model accuracy.
