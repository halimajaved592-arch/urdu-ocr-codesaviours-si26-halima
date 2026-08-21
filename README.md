# Urdu OCR — Code Saviours SI-26

An OCR application that takes an Urdu text image as input and extracts the text using a TrOCR-based deep learning model.

## Why This Matters

Urdu OCR is challenging because Urdu uses a connected Nastaliq writing style and has fewer high-quality OCR resources than English. This project explores how deep learning and image-to-text models can be used to automatically convert Urdu text from images into editable Unicode text. The project was developed as part of the Code Saviours SI-26 Machine Learning Internship.

## Live Demo

🚀 **Hugging Face Space:**  
https://huggingface.co/spaces/halimajaved592/urdu-ocr

## Loom Link
https://www.loom.com/share/7c8778a81c0441c7b85842053daed63e

The demo provides a simple interface where users can upload an Urdu image and receive extracted text.

## How It Works

1. The user uploads an image containing Urdu text.
2. The image is processed and converted into the format required by the OCR model.
3. A TrOCR-based Vision Encoder-Decoder model analyzes the image and generates text.
4. The generated tokens are decoded into readable Urdu Unicode text and displayed in the Gradio interface.

## Dataset

The project dataset contains **200 Urdu image-text pairs**.

- **Total images:** 200
- **Training images:** 160
- **Testing images:** 40
- **Format:** PNG/JPG images with corresponding Urdu text labels
- **Labels file:** `labels.csv`
- **Columns:** `image`, `text`

Example:

| Image | Text |
|---|---|
| `data/processed/0.png` | پشاور،بنوں (نمائندہ جنگ،اے ایف پی)... |
| `data/processed/1.png` | اسکے ساتھ ملحقہ علاقے کے عوام نے بجلی و گیس... |

## Results

The project was evaluated on a held-out test set of **40 images**.

The current model successfully completes the complete OCR pipeline — image preprocessing, Urdu tokenization, model generation, and text decoding — but the current 200-image training dataset is not large enough to achieve reliable Urdu OCR accuracy.

Therefore, **no artificial accuracy or F1 score is reported**.

During testing, the model produced Urdu-character output but still made substantial recognition errors. This limitation was identified during evaluation and documented as part of the project.

For comparison, published Urdu TrOCR work also reports that dataset size is a major limitation for Urdu OCR performance. One SI-26 Urdu TrOCR model reports a CER of 0.52 on its evaluation set and notes that larger datasets are needed for substantially better accuracy.  
Source: https://huggingface.co/qandeelasim13/urdu-ocr-trocr-si26

## Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- TrOCR
- Vision Encoder-Decoder
- Google Colab
- Tesla T4 GPU
- Gradio
- Hugging Face Spaces
- Google Drive

## Project Structure

```text
urdu-ocr/
│
├── data/
│   ├── processed/
│   │   └── Urdu images
│   └── labels.csv
│
├── notebooks/
│   └── Urdu OCR training and evaluation notebook
│
├── app.py
├── requirements.txt
└── README.md
How to Run Locally

Clone the repository:

git clone https://github.com/halimajaved592-arch/urdu-ocr-codesaviours-si26-halima.git
cd urdu-ocr-codesaviours-si26-halima

Install the required packages:

pip install torch torchvision
pip install transformers
pip install sentencepiece
pip install pillow
pip install gradio

Run the application:

python app.py

The Gradio interface will open locally in your browser.

Hugging Face Model

The trained model repository is available here:

https://huggingface.co/halimajaved592/urdu-ocr-trocr

Future Improvements
Increase the size and diversity of the Urdu OCR dataset.
Add more Nastaliq fonts and writing styles.
Include multi-line Urdu documents.
Apply stronger image preprocessing and augmentation.
Fine-tune the model using a larger Urdu OCR dataset.
Evaluate using Character Error Rate (CER) and Word Error Rate (WER).
Improve the live demo's OCR accuracy and robustness.
Built By

Halima Javed | Code Saviours SI-26 | 2026
