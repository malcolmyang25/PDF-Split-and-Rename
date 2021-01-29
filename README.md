# PDF-Split-and-Rename

#### The PDF information page extract is using the Tesseract. 

This Python Notebook is for PDF invoice processing, which includes Split the PDF into invididual file and Rename the PDF file using with information on first page


----------------------------------------------------

### The initialization guide lists below:
1. Install tesseract using windows installer available at: https://github.com/UB-Mannheim/tesseract/wiki

2. Note the tesseract path from the installation. Default installation path at the time of this edit was: C:\Users\USER\AppData\Local\Tesseract-OCR.
It may change so please check the installation path.

3. pip install pytesseract

4. Set the tesseract path in the script before calling image_to_string:
pytesseract.pytesseract.tesseract_cmd = r'C:\Users\USER\AppData\Local\Tesseract-OCR\tesseract.exe'


----------------------------------------------------
### PDF file error handle

```
PdfReadWarning: Invalid stream (index 0) within object 62 0: Stream has ended unexpectedly [pdf.py:1128]
```
When in strict mode, PyPDF2 quits when encountering this stream error and throws a PdfReadError. When strict is False, it ignores this error but instead gives a warning like you saw (then continues with rest of program as normal).

```
input = PdfFileReader([your file], strict = False)
```
