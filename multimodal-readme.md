# Multimodal Image-to-Text Analyzer

A robust solution for extracting and analyzing text content from images using state-of-the-art multimodal large language models.

## Features

- Image text extraction with high accuracy
- Support for multiple image formats (PNG, JPEG, TIFF, WebP)
- Multi-language text recognition
- Structured output in JSON format
- Batch processing capabilities
- Easy-to-use REST API

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



## Usage Examples

### Basic Text Extraction
```python
from multimodal_analyzer import ImageAnalyzer

analyzer = ImageAnalyzer()

# Extract text from image
result = analyzer.extract_text("receipt.jpg")
print(result.text)
```

### Advanced Usage with Custom Settings
```python
analyzer = ImageAnalyzer(
    model_name="multimodal-llm-large",
    device="cuda",
    confidence_threshold=0.8
)

result = analyzer.extract_text(
    "document.png",
    return_confidence=True,
    return_bounding_boxes=True
)
```

## API Reference

### ImageAnalyzer Class

#### Methods

- `extract_text(image_path: str, **kwargs) -> TextResult`
- `batch_process(image_paths: List[str], **kwargs) -> List[TextResult]`
- `analyze_layout(image_path: str) -> LayoutResult`

#### Parameters

- `model_name`: clip-vit-large-patch14 
- `device`: Computing device ("cuda" or "cpu")
- `confidence_threshold`: Minimum confidence score for text detection

