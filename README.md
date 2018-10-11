# ESE519_Lab3_Part4

In this part, an accelerometer is interfaced with the LCD to control the left paddle instead of using the touchscreen. In the meantime, the program for the computer is created to control the right paddle automatically.

The accelerometer is interfaced with LCD using ADC. As we only use the x-axis output from the accelerometer, the ‘x’ pin of the accelerometer is connected to the ADC input of Arduino. When the accelerometer is put horizontally, the ADC value is 333 in average. So, we clear the original paddle and draw a new paddle one pixel below when the ADC value is larger than 333 or clear the original paddle and draw a new paddle one pixel above when ADC value is less than 333.

The computer control program is triggered when the x coordinate of the ball is detected larger than 63, which means the ball is in the right half of the court. The right paddle is controlled to move 2 pixels up or down according to the relative position with the ball in each iteration.
