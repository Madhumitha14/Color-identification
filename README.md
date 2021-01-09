# **The sparks foundation Task 1:  Color Identification in Images**

## **Task Description:**
Implement an image color detector which identifies all the colors in an image

## **Solution**

In this task, we implement an image color detector which automatically tells us the name of the color detected  by double-clicking on any part of the image.
The dataset used(csv file)  cosists of five columns : colour, name of the colour, hexadecimal code for the colour and the three channels red, green and blue.
The CSV file contains in total of 865 rows of different shades of colour and its hexadecimal values.
A colourful image has been taken from the internet for this task.

First the image is read using the OpenCV function imread() and the image is resized so that it properly fits the window.
Then the pandas library is used, which is very helpful  when we need to perform various operations on data files like CSV.
pd.read_csv() reads the CSV file and loads it into the pandas DataFrame. 
A window is created on which the input image will be displayed and we set a callback function - draw_function  which will be called when the mouse action occurs.
The draw_function is then described, whose main purpose check if the event is double-clicked, then the r,g,b values along with x,y positions of the mouse are calculated and set.
Colour values are compared with the RGB values of CSV file and those values with a minimum absolute difference are picked as our colour
Using the cv2.imshow() function, we draw the image on the window. 
Finally, When the user double clicks the window, a rectangle is drawn within the image to show up the RGB values and the associated colour with the value.
