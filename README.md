# Invoice-Data-Extraction-Verification-from-Scanned-PDFs

## Overview

This project automates the extraction and validation of structured data from unstructured invoice PDFs. It combines **OCR**, **LLM-based processing**, and **rule-based validation** to accurately extract:

- General invoice metadata (e.g., invoice number, date, GSTINs)
- Line items (description, HSN code, quantity, unit price, total)
- Tax, discount, and final total
- Confidence scores and consistency validations

---

## Key Features

- ✅ OCR-based text extraction using **Tesseract**
- ✅ Semantic parsing via **Google Gemini Pro**
- ✅ Field-level confidence scoring and validation
- ✅ Line-item arithmetic verification
- ✅ Export to Excel, JSON, and log reports

---

## Tech Stack

- **OCR**: `pytesseract`, Tesseract-OCR
- **PDF Conversion**: `pdf2image`, `Pillow`
- **Image Processing**: `OpenCV`
- **LLM**: Google Gemini Pro (API)
- **Data Handling**: `pandas`, `re`, `word2number`
- **Output**: Excel (`xlsxwriter`), JSON, text logs

---

## Project Structure
project/
│
├── input/
│ └── 1WhatsApp Image.pdf # Input invoice PDF
│
├── output/
│ ├── general_info.json
│ ├── table_contents.json
│ ├── tax_info.json
│ ├── field_verification.json
│ ├── calculated_summary.json
│ ├── general_info_validated.xlsx
│ ├── table_contents_validated.xlsx
│ └── validation_log.txt
│
├── invoice.ipynb # Main script (OCR + validation) & Gemini-based info extractor
├── requirements.txt
└── README.md


---

## Installation

### Prerequisites

- Python 3.8+
- Tesseract-OCR installed locally  
  [Download Tesseract](https://github.com/tesseract-ocr/tesseract)

### Install Python Dependencies

```bash
pip install -r requirements.txt
