
**Finding Lane Lines on the Road**

### Reflection

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
Adalberto Gonzalez

SDC Program Feb 2017

#### My pipeline consists in 8 steps
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


 
### 2.  potential shortcomings with my current pipeline
<img src="./examples/y-miss.png " width="380" />
 <figcaption>
 <p></p> 
 <p style="text-align: center;"> "One potential shortcoming would be what would happen when we have a light surface where white lines are present like here where im having trouble finding white lines in this surface"</p> 
 </figcaption> 


### 3. Suggest possible improvements to your pipeline

<img src="./examples/y-miss.png " width="380" />
 <figcaption>
 <p></p> 
 <p style="text-align: center;"> "a possible improvement could be adding a validation in case i lost the slope i could maintaint the previous one
 another possible improvement could be use a curve function to fit the line instead of straight line one" </p> 
 </figcaption>
 


```python

```
