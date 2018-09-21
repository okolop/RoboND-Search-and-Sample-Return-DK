# RoboND-Search-and-Sample-Return-DK
This repository is my submission of Search and Sample Return project for Robotics Nano Degree program from Udacity. 
## Rubric Points

### Writeup / README

#### 1. Provide a Writeup / README that includes all the rubric points and how you addressed each one.  You can submit your writeup as markdown or pdf.  

This is the Writeup/README file.

### Notebook Analysis

#### 1. Run the functions provided in the notebook on test images (first with the test data provided, next on data you have recorded). Add/modify functions to allow for color selection of obstacles and rock samples.

The first problem I ran into was updating the Rover in perception_step function in perception.py. After days of googling, I found out that I have to call Rover instance/object from driving_rover.py file and define it with whatever of the rover it was that I had to update. 
Knowing that, I had to do perspect_transform() only once, but I had to perform color_thresh() function couple times. I updated the perspect_transform() by adding in another cv2.warpPerspective just like one for warped, but this time I merely created a copy of the image array with red color channel. When defining color threshold for obstacle(wall) I subtracted 1 from the first color_thresh at rgb = (160, 160, 160), which represents none-lit part of the binary image, and set that as the obstacle. 

