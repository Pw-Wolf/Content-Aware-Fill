# Content Aware Fill

This project demonstrates the "Content-Aware Fill" technique, also known as inpainting, using biharmonic functions from the `scikit-image` library. The script takes a damaged image and a mask indicating the area to be repaired, and it generates a restored image.

## Project Description

The goal of this project is to fill in missing or damaged parts of an image. This is achieved by analyzing the pixels surrounding the damaged area and smoothly propagating them to fill the gap. The process utilizes the `inpaint_biharmonic` function, which is effective for repairing small, irregular defects in images.

## How It Works

The script follows these steps:

1.  **Load Images**: The original (damaged) image and a black-and-white mask are loaded.
2.  **Prepare Mask**: The mask is converted into a binary (boolean) format, where white areas (or values greater than 0.5) indicate the region to be filled. The script also ensures the mask is two-dimensional, even if it was originally loaded as a three-channel (RGB) image.
3.  **Biharmonic Inpainting**: The core step is the application of the `restoration.inpaint_biharmonic` function. This function solves the biharmonic equation ($\Delta^2 f = 0$) to find the smoothest possible interpolation to fill the masked area.
4.  **Display Results**: Finally, the script displays the original and restored images side-by-side for comparison.

## Dependencies

To run this project, you need Python 3 and the following libraries:

-   `scikit-image`
-   `numpy`
-   `matplotlib`

You can install them using `pip`:

```bash
pip install scikit-image numpy matplotlib
```
