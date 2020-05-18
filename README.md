
The project provides a script to read an image and based on the dimensions of a reference object find the dimensions of other objects in a scene. The reference object must be the leftmost object in the scene. In sample images given, a box of dimension 2cm x 2cm is taken as a reference object.

For any other reference object provide actual width of the object. (change in file 'object.py')

## Getting Started

### Prerequisites
Python 3
Pip
OpenCV
Numpy

Other prerequisites:
- pip install numpy
- pip install opencv-python

## Algorithm
1. Image pre-processing
  - Read an image and convert it it no grayscale
  - Blur the image using Gaussian Kernel to remove un-necessary edges
  - Edge detection using Canny edge detector
  - Perform morphological closing operation to remove noisy contours

2. Object Segmentation
  - Find contours
  - Remove small contours by calculating its area (threshold used here is 100)
  - Sort contours from left to right to find the reference objects
  
3. Reference object 
  - Calculate how many pixels are there per metric (centi meter is used here)

4. Compute results
  - Draw bounding boxes around each object and calculate its height and width

## Results

![Result](/Detected%20object/1.png)
![Result](/Detected%20object/3.png)






 

