# UAS_image_classification
#This model classified objects into categories based on their color.
Model Initialization:

The YOLO model is loaded using YOLO("best.pt").

Image Processing:

Images are loaded using cv2.imread() and checked for errors.

Detection:

The model detects fruits in both images with a confidence threshold of 0.6 and an IoU threshold of 0.7.

Bounding Box Extraction:

A helper function (extract_fruits()) processes the detection results to extract bounding boxes, class IDs, and confidence scores.

IoU Calculation:

The calculate_iou() function computes the overlap between two bounding boxes to identify duplicates.

Unique Fruit Identification:

Fruits from the back image are compared with those from the front image. Non-overlapping fruits are added to the final count.

Output:

The total number of unique fruits is printed, and the detection results are displayed.

Requirements
Python 3.x

Libraries:

ultralytics (for YOLO)

opencv-python (for image processing)

Pre-trained YOLO model (best.pt)

Usage
Places the images (front_view.jpg and back_view.jpg) in the project directory.
python fruit_detection.py


To summarize:

Detect fruits in both images.

Count unique fruits.

Display the results with bounding boxes.


