# PDF Reader

A simple Python script that extracts text from PDF files using the pypdf library.

## Description

This project provides a straightforward way to extract text content from PDF documents. The script reads a PDF file and outputs all the text content to the console.

## Features

- Extract text from all pages of a PDF document
- Simple and lightweight implementation
- Uses the reliable pypdf library

## Requirements

- Python 3.x
- pypdf library

## Installation

1. Clone or download this repository
2. Install the required dependency:
   ```bash
   pip install pypdf
   ```

## Usage

1. Place your PDF file in the same directory as the script
2. Update the filename in `pdfReader.py` (currently set to "US_Employee_Policy.pdf")
3. Run the script:
   ```bash
   python pdfReader.py
   ```

The extracted text will be printed to the console.

## Example

```python
from pypdf import PdfReader

# Extract text from the PDF
reader = PdfReader("your_document.pdf")

# Extract text from all pages
document_text = ""
for page in reader.pages: 
    document_text += page.extract_text()

print(document_text)
```

## Customization

To use with different PDF files, simply change the filename in the `PdfReader()` constructor:

```python
reader = PdfReader("your_pdf_file.pdf")
```

## Notes

- The script currently processes "US_Employee_Policy.pdf" - make sure this file exists in the same directory or update the filename accordingly
- Text extraction quality may vary depending on the PDF's structure and format
- For password-protected PDFs, additional authentication steps would be required

## License

This project is open source and available under the MIT License.