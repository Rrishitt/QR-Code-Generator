# QR Code Generator (Python)

A minimal command-line tool that converts any URL into a QR code image. The script uses the `qrcode` Python library to generate the QR and saves it as a PNG file with a user-specified filename. 

---

## Features

* Converts any URL into a QR code.
* Saves output as a PNG file.
* Automatically adds `.png` if the user doesn’t include it.
* Simple, clean, and beginner-friendly.

---

## How It Works

1. Prompts the user for:

   * A URL
   * The file name to save the QR code
2. Ensures the filename ends with `.png`:

   ```python
   if not(filename.endswith(".png")):
       filename += ".png"
   ```


3. Generates the QR using:

   ```python
   img = qrcode.make(url)
   ```


4. Saves the image to disk:

   ```python
   img.save(filename)
   ```

---

## Installation

### Install the QR code library:

```bash
pip install qrcode[pil]
```

---

## Usage

Run the script:

```bash
python main.py
```

Example interaction:

```
Enter your url: https://example.com
Filename you want to save it as: myqr
```

Output generated:

```
myqr.png
```

---

## Requirements

* Python 3.x
* `qrcode` library
* Pillow (installed automatically with `qrcode[pil]`)

---

