# Screenshot to text transformer Python

This python script was written to solve a very specific problem I had: I had a lot of screenshots that only contained text and needed to put them together in one single file, preferable `.docx`.

## Technologies used

- Tesseract OCR
- pytesseract
- Pillow

## Installation

### Tesseract

Make sure you have the [Tesseract OCR](https://tesseract-ocr.github.io/tessdoc/Installation.html) installed, otherwise it wouldn't work.

Ubuntu:

```
sudo apt install tesseract-ocr
sudo apt install libtesseract-dev
```

Mac:

```
brew install tesseract
```

Windows: Best to use the [installer by UB Mannheim](https://github.com/UB-Mannheim/tesseract/wiki).

### Python dependencies

To install the necessary python dependencies, run the following:

```
pip install -r requirements.txt
```

## Usage

In the code, change the following lines (lines 5 and 7):

```python
dir_path = (r'<absolute-path-to-screenshots_folder>')

pytesseract.pytesseract.tesseract_cmd = r'<absolute-path-to-tesseract-executable>'
```

The second line is only necessary if you did not add `Tesseract` to `PATH`.

Afterwards you can just run:

```
python3 main.py
```

You will get prompted to give the output file a name (without the `.docx` extension) and that's it! The generated file will get saved to the current directory.
