# OCR Text Detection with OpenCV and EasyOCR

This repository contains a Python script for detecting and displaying text in images using OpenCV and EasyOCR. The script reads an image, uses EasyOCR to detect text, and then visualizes the detected text by drawing bounding boxes and labels on the image. The processed image is displayed using Matplotlib.

## Features

- **Text Detection**: Utilizes EasyOCR to detect text in images with support for the English language.
- **Visualization**: Uses OpenCV to draw bounding boxes and text labels around detected text.
- **Customizable Threshold**: Allows setting a confidence threshold to filter out low-confidence text detections.
- **GPU Support**: EasyOCR can leverage GPU for faster text detection.

## Requirements

- Python 3.x
- OpenCV
- EasyOCR
- Matplotlib
- NumPy

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/ocr-text-detection.git
   cd ocr-text-detection
   ```

2. Install the required packages:
   ```sh
   pip install opencv-python-headless easyocr matplotlib numpy
   ```

## Usage

1. Place the image you want to process in a known directory.

2. Update the `image_path` variable in the script with the path to your image:
   ```python
   image_path = "path/to/your/image.jpg"
   ```

3. Run the script:
   ```sh
   python detect_text.py
   ```

## Example

Here's an example of how the script works:

- The script reads the image specified in `image_path`.
- It uses EasyOCR to detect text in the image.
- For each detected text, if the confidence score is above the specified threshold, a bounding box and label are drawn on the image.
- The processed image is displayed using Matplotlib.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

This repository provides a simple yet effective approach to text detection in images, leveraging the power of EasyOCR and OpenCV. Whether you're working on a personal project or developing a prototype for a larger application, this script can serve as a valuable tool for OCR tasks.
