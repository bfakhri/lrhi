# Low Resolution Haptic Interface API 

Simple API for communicating with the LRHI to draw images onto the Low Resolution Haptic Display (LRHD). 

### LRHI Block Diagram
![alt text](https://github.com/bfakhri/lrhi/blob/master/images/lrhd_block_diag_colored.png "Low Res Haptic Interface Block Diagram")

# Software Requirements

Python3 

Numpy 
OpenCV for Python3
struct
serial
threading 
time

# Usage Example - Drawing Zeros to LRHD

from lrhd import lrhd
import numpy as np
import time

### Create an instance of the LRHD
hap_disp = lrhd()

### Get the dimension of the display
dims = (hap_disp.y_dim, hap_disp.x_dim)

### Clear the display
hap_disp.clear_display()

### Warms up the display
hap_disp.warmup()

### Scans the display by firing each motor sequentially
for i in range(dims[0]*dims[1]):
    # Create a blank haptic image 
    image = np.zeros(dims, np.uint8)
    # Lights up one motor
    image.flat[i] = 255
    # Sends the haptic image to the LRHD
    hap_disp.draw(image)
    # Delay so it can be felt
    time.sleep(0.4)


### Clear the display
hap_disp.clear_display()

### End script after 10 seconds 
time.sleep(10)

# LRHI


### Low-Res Haptic Display
![alt text](https://github.com/bfakhri/lrhi/blob/master/images/front_chair.jpg "Low Res Haptic Display")

### Low-Res Haptic Display Side View 
![alt text](https://github.com/bfakhri/lrhi/blob/master/images/array_side.png "Low Res Haptic Display")

