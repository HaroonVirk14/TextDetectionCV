import cv2
import easyocr
import matplotlib.pyplot as plt
import numpy as np

# Specify the path to the image
image_path = "C:/Users/Haroon Virk/Downloads/shutterstock_1785217352-1-750x430.jpg"

# Read the image using OpenCV
img = cv2.imread(image_path)

# Initialize the EasyOCR reader with English language support and GPU usage enabled
reader = easyocr.Reader(['en'], gpu=True)

# Detect text in the image
detected_text = reader.readtext(img)

# Set the confidence threshold
confidence_threshold = 0.25

# Iterate through the detected text
for idx, text_info in enumerate(detected_text):
    print(text_info)

    bbox, text, score = text_info

    # Draw a rectangle and put text if the confidence score is above the threshold
    if score > confidence_threshold:
        cv2.rectangle(img, tuple(bbox[0]), tuple(bbox[2]), (0, 255, 0), 5)
        cv2.putText(img, text, tuple(bbox[0]), cv2.FONT_HERSHEY_COMPLEX, 0.68, (255, 0, 0), 2)

# Convert the image from BGR to RGB and display it using Matplotlib
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.show()
