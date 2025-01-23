# Check-Scanner
Optical Character Recognition (OCR) scanner of CTS-2010 standard bank cheque using EAST text detector and pytesseract with capabilities to detect amount and account number in the cheque. 
Anaconda Python - OpenCV is used for image processing.

## Final Draft.ipynb Explanation

The `Final Draft.ipynb` notebook demonstrates the complete workflow for detecting and extracting text from cheque images. Below is a detailed explanation of the steps performed:

1. **Import Libraries and Read Image**:
   - Import necessary libraries such as `skimage`, `matplotlib`, `imutils`, `cv2`, and `numpy`.
   - Read the cheque image and process it to find the bounding box of the cheque.
   - Display the cropped cheque image.

2. **Resize Image**:
   - Import additional libraries (`imutils`, `pytesseract`, `cv2`, `time`, `os`).
   - Read and resize the cheque image for further processing.
   - Calculate the resizing ratios.

3. **Display Original Image**:
   - Display the original cheque image using OpenCV.

4. **Load EAST Text Detector**:
   - Load the pre-trained EAST text detector model.
   - Prepare the image as a blob and perform a forward pass to get the scores and geometry of the detected text.
   - Print the time taken for text detection.

5. **Extract Bounding Boxes**:
   - Process the scores and geometry to extract bounding boxes for detected text regions.
   - Filter out weak detections based on a confidence threshold.

6. **Non-Maxima Suppression**:
   - Apply non-maxima suppression to the bounding boxes to remove overlapping boxes.
   - Extract text from the detected regions using pytesseract.
   - Print the detected text along with the bounding box coordinates.

7. **Draw Bounding Boxes**:
   - Draw bounding boxes on the original image and display it.

8. **Calculate Account Number Region**:
   - Calculate the coordinates for the account number region on the cheque.
   - Print the coordinates.

9. **Calculate Amount Region**:
   - Calculate the coordinates for the amount region on the cheque.
   - Print the coordinates.

10. **Extract Account Number and Amount**:
    - Use regular expressions to extract the account number and amount from the detected text regions.
    - Print the extracted account number and amount.

11. **Draw Bounding Boxes on Different Image**:
    - Draw bounding boxes on a different image (`check10.jpg`) and display it.

The notebook provides a comprehensive guide to detecting and extracting text from cheque images, including preprocessing, text detection, and text extraction using OCR.
