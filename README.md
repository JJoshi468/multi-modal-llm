# Multimodal Analyzer Using Langchain

A robust solution for extracting and analyzing text content from images and pdfs using state-of-the-art multimodal large language models.

## Features

- Image text extraction with high accuracy
- Support for multiple image formats (PNG, JPEG)
- Multi-language text recognition

## Installation

```bash
pip install langchain langchain-community langchain-huggingface
```


## Dependencies

- Python 3.8+
- PyTorch >= 2.0
- transformers >= 4.30.0
- Tesseract
- pytesseract (set path from code)


#### Parameters

- `model_name`: clip-vit-large-patch14 
- `device`: Computing device ("cuda" or "cpu")
- `confidence_threshold`: Minimum confidence score for text detection

