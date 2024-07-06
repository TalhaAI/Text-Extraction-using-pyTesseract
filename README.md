# OCR System for Image and PDF Processing

This project provides a comprehensive Optical Character Recognition (OCR) system that processes both images and PDF files to extract text. The system uses Tesseract OCR and OpenCV for preprocessing tasks, enhancing the accuracy of text recognition.

## Pipeline Overview

1. **File Upload**: Users upload images or PDFs using Google Colab's file upload interface.
2. **File Type Classification**: The script categorizes the uploaded files into image files and PDF files.
3. **Image Processing**: Each image (or page of a PDF) undergoes several preprocessing steps to enhance text extraction accuracy.
4. **Text Detection**: The processed image is analyzed to detect text regions.
5. **Text Extraction**: Detected text regions are processed with Tesseract OCR to extract text.
6. **Output**: The extracted text is printed, and images with bounding boxes around detected text regions are displayed.

## Preprocessing Steps

1. **Grayscale Conversion**: Convert the image to grayscale for better processing.
2. **Noise Reduction**: Apply a bilateral filter to reduce noise while keeping edges sharp.
3. **Adaptive Thresholding**: Convert the grayscale image to a binary image using adaptive thresholding.
4. **Morphological Operations**: Apply morphological closing to close small gaps in the binary image.

## Configuration Settings

- **Tesseract Path**: The path to the Tesseract executable is set using `pytesseract.pytesseract.tesseract_cmd`.
- **Adaptive Thresholding Parameters**: Block size and constant used for adaptive thresholding.
- **Morphological Operations**: Kernel size and iterations for morphological closing.
- **Contour Detection**: Contour area threshold for detecting text regions.
- **Tesseract OCR Settings**: OCR engine mode (OEM) and page segmentation mode (PSM).
