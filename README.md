# Urdu OCR Project | Code Saviours SI-26 | Halima Javed

This repository contains my work for the ML/AI SI-26 Urdu OCR Internship project at Code Saviours.

Week 1:
- Environment setup
- Dataset collection
- Google Colab notebook

## Research Summary

OCR (Optical Character Recognition) is a technology that converts text from images into editable digital text. Urdu OCR is more challenging than English OCR because Urdu is written from right to left, characters change shape depending on their position, and many letters are distinguished only by dots. Urdu OCR has many practical applications, including digitizing books, newspapers, historical records, and government documents.

## Week 2 – Image Preprocessing & OCR Testing

### Tasks Completed
- Preprocessed Urdu images using OpenCV.
- Converted images to grayscale.
- Applied Gaussian blur for noise reduction.
- Applied thresholding to improve text visibility.
- Saved processed images in `data/processed/`.

### OCR Testing
- Tested the processed images using Tesseract OCR with pytesseract.
- Compared the OCR output with the original Urdu text.

### Gap Analysis
Tesseract showed poor performance on Urdu text because Urdu uses a cursive script with connected characters. Many words were recognized incorrectly or not recognized at all, demonstrating the need for a specialized Urdu OCR model.
