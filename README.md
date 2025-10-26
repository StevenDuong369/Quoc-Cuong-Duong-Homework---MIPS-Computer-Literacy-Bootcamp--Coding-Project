Here’s a professional and clear **README** file for your pixelation/blur script:

---

# Pixelate Image Script

## Overview

This Python script applies a **pixelation blur effect** to an image. It works by dividing the image into a grid of blocks and replacing each block’s pixels with the **average color** of that block. The result is a stylized, mosaic-like version of the original photo.

---

## Features

* Pixelates an image using a grid-based approach.
* Grid block size is defined as **5% of the image’s width and height**, automatically scaling with the image size.
* Supports any RGB image format.
* Saves the output as a new image file and displays it automatically.

---

## Requirements

* Python 3.x
* [Pillow (PIL)](https://pypi.org/project/Pillow/) library

Install Pillow if you haven’t already:

```bash
pip install pillow
```

---

## Usage

1. Place your image in the same folder as the script and name it `photo.jpg` (or update the filename in the script).
2. Run the script:

```bash
python pixelate_blur.py
```

3. The script will:

   * Load the image.
   * Divide it into a grid of blocks (5% of width and height).
   * Compute the average color for each block.
   * Fill each block with the average color.
   * Display the resulting image.
   * Save the output as `blured_photo.jpg`.

---

## How It Works

1. **Load Image**: Opens the image and converts it to RGB mode.
2. **Define Block Size**: Sets each block to 5% of the image dimensions, ensuring blocks scale with image size.
3. **Process Each Block**:

   * Sum all red, green, and blue values in the block.
   * Compute the average color.
   * Replace all pixels in the block with the average color.
4. **Save Result**: Outputs the processed image to a new file.

---

## Example

Original image:

```
photo.jpg
```

Pixelated output:

```
blured_photo.jpg
```

---

## Notes

* You can adjust the block size by changing the divisor (currently `width // 20` and `height // 20` which means dividing the image into a grid of 20 blocks) to make pixelation finer or coarser.
* The script automatically ensures block size is at least 1 pixel to handle very small images.

