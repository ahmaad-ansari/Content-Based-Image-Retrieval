# Content-Based Image Retrieval (CBIR)

## Overview

This project is a Content-Based Image Retrieval (CBIR) system built using Python and PyQt5. CBIR is a technique that allows you to search for images in a database based on their visual content. In this project, you can browse images, generate image barcodes, and search for similar images using a CBIR approach.

## Getting Started

To run this project, you will need to follow these steps:

1. Clone or download this repository to your local machine.

2. Ensure you have the necessary dependencies installed. You can install them using pip:

   ```
   pip install pillow PyQt5 pandas numpy
   ```

3. Open a terminal and navigate to the project directory.

4. Run the `main.py` file to start the application:

   ```
   python main.py
   ```

5. The application window will appear, and you can start using the CBIR system.

## Features

### 1. Browse Images

- Click the "Browse" button to select an image file (supported formats: `.png`, `.jpg`, `.jpeg`, `.bmp`).

- The selected image will be displayed in the GUI.

### 2. Generate Image Barcodes

- After selecting an image, click the "Generate Barcode File" button to create a barcode for the selected image.

- The barcode is created using the image's visual content.

- The barcode is stored in a CSV file named "BARCODES.csv."

- The image file path is stored in a CSV file named "IMAGEPATH.csv."

### 3. Retrieve Similar Images

- After generating a barcode for an image, the system can retrieve visually similar images based on the barcode.

- The system uses a CBIR approach to calculate the Hamming distance between the barcode of the selected image and those of other images in the database.

- The image with the closest barcode (lowest Hamming distance) is displayed as the result.

## Usage

1. Browse for an image by clicking the "Browse" button and selecting an image file.

2. Click the "Generate Barcode File" button to create a barcode for the selected image.

3. The barcode is saved in the "BARCODES.csv" file, and the image file path is saved in the "IMAGEPATH.csv" file.

4. You can now retrieve similar images by selecting an image and clicking the "Retrieve Similar Images" button.

5. The system will display the visually most similar image from the database.

## Important Notes

- Make sure to change the `rootDir` variable in the code to specify the root directory of your image database.

- The application assumes that you have a directory structure with image files in subdirectories under the specified root directory.

- The image retrieval process uses a simple Hamming distance algorithm for demonstration purposes. You can explore more advanced similarity metrics for a production system.

## Dependencies

- Python 3.10
- PyQt5
- Pillow (PIL)
- pandas
- numpy
