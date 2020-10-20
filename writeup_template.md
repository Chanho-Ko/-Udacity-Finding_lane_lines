# **Finding Lane Lines on the Road** 
---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Apply a pipeline for the video
* Modify the draw_lines() function for creating a single line of right and left lane


[//]: # (Image References)

[image_in]: ./test_images/solidWhiteRight.jpg "Input image"
[image_out]: ./test_images_output/solidWhiteRight.jpg "Output image"

---

### Reflection

### 1. Description of pipeline.

My pipeline consisted of 5 steps. 
* Input image is converted into gray scale image, and filtered with Gaussian smoothing.
* Detection canny edges with proper low and high thresholds.
* Masked edge image is created baseed on four vertices that we are interested in.
* Creating line image that includes all of lines calculated by Hough transform.
* Draw a single line on the left and right lanes by averaging and extrapolation.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function.
The left and right line is decided by the sign of slope of the line.
x and y points are sumed up and the average of points and slope are calulated.
Based on the point and slope, the line is exprapolated based on the range of y coordinate.

The result for a example image is shown below:

![alt text][image_in]
![alt text][image_out]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
