# Road-lane-detection
An AI-ML project built with Python and OpenCV for detecting road lane lines in real-time. Using Canny edge detection and Hough Line Transform, the system identifies and highlights lane boundaries from images and videos, contributing to safer driving solutions.
This project implements a basic road lane line detection system using computer vision techniques in Python. The system identifies lanes on the road by applying Canny edge detection, Hough Line Transformation, and drawing the detected lanes on images or video frames.
# FEATURES
Lane Detection from Static Image: Detects lanes from a given road image.
Lane Detection from Video: Continuously detects lanes from each frame of a video.
Edge Detection: Utilizes the Canny edge detection algorithm for detecting edges in the image.
Hough Transform for Line Detection: Uses the Hough Line Transform to detect lanes.
Averaging Lane Lines: Combines multiple line segments into single representative lane lines.
# REQUIREMENTS
Ensure you have Python 3.x installed on your system. Additionally, the following Python libraries are required:
OpenCV (opencv-python)
NumPy
Matplotlib (only used for debugging or visualizing)
# CODE OVERVIEW
# Key Functions
make_coordinates(image, line_parameters): Converts the slope and intercept of a line to coordinates for drawing.

average_slope_intercept(image, lines): Averages the detected lane lines to smooth out any noise or deviations.

canny(image): Converts the image to grayscale, applies a Gaussian blur, and uses Canny edge detection to highlight lane edges.

display_lines(image, lines): Draws the detected lines (lane markings) on a blank image.

region_of_interest(image): Applies a mask to focus only on the area of the image where lanes are expected to be found (a triangular region).

# Main Workflow
Image Loading: The script loads a static image or captures video frames.
Canny Edge Detection: The canny() function is used to detect edges.
Masking the Region of Interest: The lane area is masked using region_of_interest().
Hough Line Transform: Lines are detected using cv2.HoughLinesP.
Averaging Lines: The lines are averaged using average_slope_intercept() to smooth out noise.
Displaying the Results: The detected lanes are displayed on the image or video.

# Example Output
The detected lane lines will be highlighted in blue on the road image or video. The processed frames or image are displayed using OpenCV's cv2.imshow function.
![Screenshot (64)](https://github.com/user-attachments/assets/00247d5a-4fb3-47f4-8870-73ad1ea6c738)
https://github.com/user-attachments/assets/4331adc9-d6ec-40ed-95ed-b3b63fb03809



