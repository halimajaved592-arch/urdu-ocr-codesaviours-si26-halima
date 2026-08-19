# Urdu OCR Project | Code Saviours SI-26 | Halima Javed

This repository contains my work for the ML/AI SI-26 Urdu OCR Internship project at Code Saviours.

## Week 1 – Environment Setup & Dataset Collection

### Tasks Completed

* Set up the development environment.
* Created the GitHub repository.
* Set up Google Colab.
* Collected Urdu OCR image data.
* Created the initial dataset and labels.

## Research Summary

OCR (Optical Character Recognition) is a technology that converts text from images into editable digital text. Urdu OCR is more challenging than English OCR because Urdu is written from right to left, characters change shape depending on their position, and many letters are distinguished only by dots. Urdu OCR has many practical applications, including digitizing books, newspapers, historical records, and government documents.

## Week 2 – Image Preprocessing & OCR Testing

### Tasks Completed

* Preprocessed Urdu images using OpenCV.
* Converted images to grayscale.
* Applied Gaussian blur for noise reduction.
* Applied thresholding to improve text visibility.
* Saved processed images in `data/processed/`.

### OCR Testing

* Tested the processed images using Tesseract OCR with pytesseract.
* Compared the OCR output with the original Urdu text.

### Gap Analysis

Tesseract showed poor performance on Urdu text because Urdu uses a cursive script with connected characters. Many words were recognized incorrectly or not recognized at all, demonstrating the need for a specialized Urdu OCR model.

## Week 3 – Dataset Preparation

### Tasks Completed

* Expanded the Urdu OCR dataset.
* Organized image and label files.
* Loaded the dataset using Python.
* Created a custom dataset/data loader.
* Prepared images for model training.
* Split the dataset into training and testing sets.

The prepared dataset contained image samples paired with their corresponding Urdu text labels.

## Week 4 – TrOCR Research & Implementation

### Tasks Completed

* Researched Transformer-based OCR models.
* Studied the Hugging Face TrOCR model architecture.
* Selected TrOCR as the main OCR approach.
* Prepared image-text pairs for TrOCR.
* Used a TrOCR processor for image preprocessing and text tokenization.
* Tested the model on Urdu OCR data.

### Why TrOCR?

TrOCR combines a Vision Transformer-based image encoder with a Transformer-based text decoder. It is designed for image-to-text recognition and provides a suitable foundation for fine-tuning on custom OCR datasets.

## Week 5 – Model Training Preparation

### Tasks Completed

* Prepared the training dataset for TrOCR.
* Converted images into the required format.
* Prepared corresponding Urdu text labels.
* Created training and testing datasets.
* Configured the processor and model.
* Prepared the training pipeline using Hugging Face Transformers and PyTorch.

### Dataset

The dataset consists of Urdu text images and their corresponding ground-truth transcriptions.

The training pipeline was designed to learn the relationship between an input Urdu image and its correct text transcription.

## Week 6 – Model Training & Testing

### Tasks Completed

* Continued the TrOCR training pipeline.
* Used Google Colab for model training.
* Utilized GPU acceleration where available.
* Tested the trained model on unseen test images.
* Compared predicted OCR text with the ground-truth text.

The model was evaluated using test samples that were not used during training.

## Week 7 – Model Evaluation

### Evaluation

The trained OCR model was evaluated by comparing the predicted Urdu text with the ground-truth labels.

Important OCR evaluation measures include:

* Character Error Rate (CER)
* Word Error Rate (WER)
* Exact Match
* Accuracy

These metrics help determine how accurately the model recognizes Urdu text from images.

### Evaluation Observation

The initial TrOCR setup showed limitations when recognizing Urdu because the original pretrained model is not specifically optimized for Urdu script. This highlighted the importance of suitable Urdu training data, preprocessing, and fine-tuning.

## Week 8 – Final Testing & Documentation

### Tasks Completed

* Finalized the dataset preparation pipeline.
* Tested the OCR model on sample images.
* Compared predictions with ground-truth Urdu text.
* Reviewed model performance.
* Documented the project workflow and findings.
* Organized the GitHub repository.
* Prepared the project for final demonstration.

### Final Project Workflow

```text
Urdu Image
    ↓
Image Preprocessing
    ↓
Dataset + Ground Truth Text
    ↓
TrOCR Processor
    ↓
TrOCR Model
    ↓
Model Training / Fine-tuning
    ↓
Test Image
    ↓
Predicted Urdu Text
    ↓
Evaluation
```

## Technologies Used

* Python
* Google Colab
* PyTorch
* Hugging Face Transformers
* TrOCR
* OpenCV
* Tesseract OCR
* pytesseract
* GitHub

## Project Structure

```text
urdu-ocr-codesaviours-si26-halima/
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── labels.csv
│
├── notebooks/
│
├── SI26-Week*.ipynb
│
├── README.md
│
└── requirements.txt
```

## Key Learning Outcomes

Through this project, I learned:

* Fundamentals of Optical Character Recognition.
* Challenges involved in Urdu OCR.
* Image preprocessing techniques using OpenCV.
* Tesseract OCR testing.
* Dataset preparation for deep learning.
* Transformer-based OCR using TrOCR.
* Hugging Face Transformers and processors.
* Model training and evaluation.
* Working with GPU environments in Google Colab.
* Using GitHub for project documentation and version control.

## Future Improvements

* Increase the size and diversity of the Urdu OCR dataset.
* Fine-tune a multilingual or Urdu-specific OCR model.
* Improve Urdu character and word recognition.
* Evaluate the model using CER and WER.
* Deploy the trained OCR model as a web application.
* Test the system on real-world Urdu documents.

## Author

**Halima Javed**

ML/AI Intern — Code Saviours SI-26
SI26-ML-HJ-032
