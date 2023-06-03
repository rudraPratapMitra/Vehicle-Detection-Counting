# Vehicle-Detection-Counting
This code represents a vehicle detection, classification, and counting system using computer vision techniques. The goal of this project is to analyze a video stream or video file and detect vehicles, classify them as cars or trucks, and count the number of vehicles moving in different directions.

Here's a breakdown of the major components and functionalities of the code:

1. Library Imports: The necessary libraries, including OpenCV (cv2), numpy, time, and a custom module named "vehicles," are imported.

2. Variable Declarations: Various variables are initialized, such as the video capture object (cap), background subtractor (fgbg), kernels for morphological operations (kernalOp, kernalOp2, kernalCl), font style for text overlay (font), a list to store vehicle objects (cars), and other parameters for counting and tracking.

3. Background Subtraction: The background subtractor (MOG2) is applied to the frame to obtain a foreground mask (fgmask), which highlights moving objects.

4. Binarization and Morphological Operations: The foreground mask is binarized using a threshold value, and morphological operations (opening and closing) are applied to remove noise and refine the binary mask.

5. Contour Extraction: Contours are extracted from the binary mask using the findContours function. Each contour represents a potential object in the frame.

6. Vehicle Detection and Tracking: For each contour, the code checks if its area exceeds a certain threshold (300 in this case) to consider it as a vehicle. It calculates the centroid of the contour and checks if it falls within the specified region of interest.

7. Vehicle Classification and Counting: If a new vehicle is detected, a vehicle object is created and added to the cars list. If an existing vehicle is matched to a contour, its coordinates are updated. 

8. Visualization and Display: The code overlays text and lines on the frame to indicate the count of vehicles and their movement directions. The frame, along with the overlays, is displayed in a window using OpenCV's imshow function.

<img width="348" alt="vehicleDetection github" src="https://github.com/rudraPratapMitra/Vehicle-Detection-Counting/assets/135310293/a7c25239-8a51-4bfc-b453-16fcf3c226f7">





