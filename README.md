# **Finding Lane Lines on the Road**

### Adalberto Gonzalez
Self-Driving Car Engineer Nanodegree Program

---

<img src="laneLines_thirdPass.jpg" width="480" alt="Combined Image" />

Overview
---

When we drive, we use our eyes to decide where to go.  The lines on the road that show us where the lanes are act as our constant reference for where to steer the vehicle.  Naturally, one of the first things we would like to do in developing a self-driving car is to automatically detect lane lines using an algorithm.

In this project I detect lane lines in images using Python and OpenCV.  OpenCV means "Open-Source Computer Vision", which is a package that has many useful tools for analyzing images.  

In this project, the key files is called P1.ipynb



#### Pipeline in 8 steps
<img src="./examples/a-ori.png " width="380" alt="Original Image" />
 <figcaption>
 <p></p> 
 <p style="text-align: center;"> "Original Image" </p> 
 </figcaption>
<img src="./examples/b-white.png " width="380" />
 <figcaption>
 <p></p> 
 <p style="text-align: center;"> "First, I converted the images to whitescale ..." </p> 
 </figcaption>
<img src="./examples/c-yellow.png " width="380" />
 <figcaption>
 <p></p> 
 <p style="text-align: center;"> "and yellow scale" </p> 
 </figcaption>
<img src="./examples/d-wy.png " width="380" />
 <figcaption>
 <p></p> 
 <p style="text-align: center;"> "and combined yellow and white " </p> 
 </figcaption>
 <img src="./examples/e-blur.png " width="380" />
 <figcaption>
 <p></p> 
 <p style="text-align: center;"> "then applied Gaussian smoothing" </p> 
 </figcaption>
<img src="./examples/f-edges.png " width="380" />
 <figcaption>
 <p></p> 
 <p style="text-align: center;"> "defined parameters for Canny and apply them" </p> 
 </figcaption>
<img src="./examples/g-roi.png " width="380" />
 <figcaption>
 <p></p> 
 <p style="text-align: center;"> "Next created a Masked edges image to get a region of interest" </p> 
 </figcaption>
<img src="./examples/h-res.png " width="380" />
 <figcaption>
 <p></p> 
 <p style="text-align: center;"> "Define the Hough transform parameters
    i defined the draw_line function
       based on the slope of each individual line diferenctiate from left to rigth and in each case
       get slope, intercepts
       and then get the averages of those parameters to draw a new line that goes could cover the area of interest and also i add a validation in the slope to avoid getting drastic slopes changes" </p> 
 </figcaption> 
<img src="./examples/h-res.png " width="380" />
 <figcaption>
 <p></p> 
 <p style="text-align: center;"> "finally blended the images to visualize the result of the lane detection on top of the original image " </p> 
 </figcaption> 


 
### Potential shortcomings with my current pipeline
<img src="./examples/y-miss.png " width="380" />
 <figcaption>
 <p></p> 
 <p style="text-align: center;"> "One potential shortcoming would be what would happen when we have a light surface where white lines are present like here where im having trouble finding white lines in this surface"</p> 
 </figcaption> 


### Possible improvements to your pipeline

<img src="./examples/y-miss.png " width="380" />
 <figcaption>
 <p></p> 
 <p style="text-align: center;"> "a possible improvement could be adding a validation in case i lost the slope i could maintaint the previous one
 another possible improvement could be use a curve function to fit the line instead of straight line one" </p> 
 </figcaption>
 

Thanks for Reading.
Adalberto Gonzalez


```python

```

