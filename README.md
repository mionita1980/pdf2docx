# Convert PDF to DOCX Using Python Lib

  * [Install PreRequisites](#install-prerequisites)
  * [Create Sample PDF](#create-sample-pdf)
  * [Convert Sample PDF to DOCX](#convert-sample-pdf-to-docx)

## Install PreRequisites

Assuming you already have python installed (if not, install python via `devbox` to avoid polluting your local environment).

Install the lib:
```bash
pip install pdf2docx
```

## Create Sample PDF

> NOTE: Skip this if you already have a PDF file.

Create a markdown file
```markdown
# Sample Document


## Sample Chapter

Sample text for this document.

![img1 image](./img1.jpg)

## Another Sample Chapter

Some more sample text for this document.  
Whatever other text.
```

Install prerequisites for creating a PDF from Markdown
- https://pandoc.org/installing.html
- https://miktex.org (you usually require a `Tex` too)

Create the PDF
```bash
pandoc sample.md -o sample.pdf
```

## Convert Sample PDF to DOCX

```bash
pdf2docx convert sample.pdf sample.docx
```

Expected output
```
[INFO] Start to convert sample.pdf
[INFO] [1/4] Opening document...
[INFO] [2/4] Analyzing document...
[INFO] [3/4] Parsing pages...
[INFO] (1/1) Page 1
[INFO] [4/4] Creating pages...
[INFO] (1/1) Page 1
[INFO] Terminated in 0.11s.
```
