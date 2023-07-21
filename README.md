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

<p align="center">
  <img src="https://github.com/IssamSayyaf/RSNA-Breast-Cancer-Detection/blob/main/images/Image%20Distribution.png" alt="alt text" width="width" height="height" />
  <br>
  <em>Figure 1: The Dataset Distribution</em>
</p>

# Methods

To design an efficient model for breast cancer detection, a well-defined pipeline can be established, encompassing pre-processing of the dataset, designing and training the model architecture, and evaluating the model's performance. The pipeline can be described in the following steps:

## i. Preprocessing

The pre-processing pipeline for the RSNA Breast Cancer Detection dataset can be summarized in the following steps:

1. **Read the DICOM images:**
   The dataset is provided in DICOM format, which requires reading and conversion into a format compatible with model processing.

2. **Crop the images:**
   To remove any background noise and reduce redundancy in the images, the breast region must be identified and cropped. Techniques such as thresholding can be employed, as exemplified in Figure 3.

3. **Normalize the pixel values:**
   Normalizing the pixel values of the images to a range of [0, 255] ensures consistent image representation and prevents model saturation.

4. **Enhance contrast:**
   Utilizing contrast enhancement techniques, such as Contrast Limited Adaptive Histogram Equalization (CLAHE), can significantly improve the visibility of breast tissue in the images. CLAHE adjusts image contrast locally while preserving overall contrast and image quality.

5. **Resize the images:**
   Ensuring uniform image dimensions is crucial for consistency and reduced computational load on the model. Therefore, resizing the images to a standardized size is essential.

6. **Save the processed images:**
   After pre-processing the dataset, saving the images in an efficient format for model training is vital. One effective method is using the TFRecord format.

Overall, the pre-processing pipeline aims to standardize image dimensions, enhance contrast, and balance the dataset, ultimately leading to an optimized dataset for model training and improved model performance, as depicted in Figure 3.

