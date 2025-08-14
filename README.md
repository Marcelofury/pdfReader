
# PDF Text Extractor

This project demonstrates how to extract text from a PDF file using the [`pypdf`](https://pypdf.readthedocs.io/) Python library. The example provided reads an employee policy document (`US_Employee_Policy.pdf`) and prints its content to the console.

## Features

- Extracts text from all pages of a PDF file.
- Concatenates the extracted text for further analysis or processing.

## Requirements

- Python 3.7+
- [`pypdf`](https://pypdf.readthedocs.io/en/latest/)

## Installation

Install the required package via pip:

```bash
pip install pypdf
```

## Usage

Place your PDF file (e.g., `US_Employee_Policy.pdf`) in the same directory as your script. Then use the following code to extract and print the text:
```python
from pypdf import PdfReader

# Extract text from the PDF
reader = PdfReader("US_Employee_Policy.pdf")

# Extract text from all pages
document_text = ""
for page in reader.pages: 
    document_text += page.extract_text()

print(document_text)
```

## Notes

- Make sure your PDF is not encrypted. If it is, you may need to handle decryption.
- The quality of extracted text depends on the source PDF (scanned documents may require OCR).

## License

This project is provided under the MIT License.
````
