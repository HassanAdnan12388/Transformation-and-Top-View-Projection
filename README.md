# Transformation-and-Top-View-Projection
Transformation and Top View Projection of images and videos using Homography and Keypoint matching techniques.
Image Transformation and Projection (SuperPoint and SuperGlue)

# Overview
This project focuses on image and video transformation using SuperPoint and SuperGlue models for keypoint extraction and matching, along with homography transformations to project static images onto dynamic video frames. The primary task is to project images (e.g., Rick and Morty) onto video frames of a monitor or a road scene, using techniques like image warping and keypoint-based matching.

# Part 1: Front View Projection 
- Implement the projection of a static image (e.g., Rick and Morty) onto a monitor using homography.
- Use SuperPoint for keypoint detection and SuperGlue for keypoint matching.
- Calculate the homography matrix and warp the image onto the monitor screen.
- Implement projection onto a video feed of the monitor, ensuring alignment with the screen throughout the video sequence.

# Task 2: Top View Projection 
- Capture an image of a road and use a satellite image for top-view projection.
- Apply segmentation to isolate the road and find the homography matrix for the projection.
- Project the road scene from a video into a top-down view using keypoint matching and homography.
- Integrate YOLO for segmentation tasks in road images and videos.


# Model Architecture
**SuperPoint**
-A neural network model for keypoint detection and description.
-Outputs keypoints and their associated descriptors, used for image matching.
**SuperGlue**
- A model that performs matching of keypoints across images based on SuperPoint outputs.
-Calculates correspondences and matches keypoints using a graph neural network approach.
**Homography Calculation**
- Using the matched keypoints from SuperPoint and SuperGlue, the homography matrix is computed using RANSAC to project one image onto another.

# Technologies Used
- PyTorch: For implementing the SuperPoint and SuperGlue models, which are based on deep learning techniques for keypoint detection and matching.
- OpenCV: Used for image processing tasks like converting to grayscale, detecting edges, finding contours, and performing homography transformations.
- NumPy: Used for handling arrays, matrices, and mathematical operations required for image and video manipulation.
- TorchVision: Used for various image preprocessing tasks such as resizing and transforming images.
- SuperPoint and SuperGlue Pretrained Models: Pretrained models for keypoint detection (SuperPoint) and matching (SuperGlue) to enable efficient and accurate transformations.
- YOLOv8: For object detection in video frames (optional, for segmentation tasks).
- FFmpeg: Used for video processing (reading video files, writing video frames).
