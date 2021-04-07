# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

# In this part, we will cover in detail the different steps needed to create our pipeline, which will enable us to identify and classify lane lines. The pipeline # itself will look as follows:
# Convert original image to HSL
# Isolate yellow and white from HSL image
# Combine isolated HSL with original image
# Convert image to grayscale for easier manipulation
# Apply Gaussian Blur to smoothen edges
# Apply Canny Edge Detection on smoothed gray image
# Trace Region Of Interest and discard all other lines identified by our previous step that are outside this region
# Perform a Hough Transform to find lanes within our region of interest and trace them in red
# Separate left and right lanes
# Interpolate line gradients to create two smooth lines
