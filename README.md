# Low Resolution Haptic Interface API 

Simple API for communicating with the LRHI to draw images onto the Low Resolution Haptic Display (LRHD). 

# Requirements

Python3 

Numpy 
OpenCV for Python3
struct
serial
threading 
time

# Usage Example - Drawing Zeros to LRHD

from lrhd import lrhd

hap_disp = lrhd()

dims = (hap_disp.y_dim, hap_disp.x_dim)

image = np.zeros(dims, np.uint8)

hap_disp.draw(image)

# LRHI

### LRHI Block Diagram
![alt text](https://github.com/bfakhri/lrhi/blob/master/images/lrhd_block_diag_colored.png "Low Res Haptic Interface Block Diagram")

### Low-Res Haptic Display
![alt text](https://github.com/bfakhri/lrhi/blob/master/images/front_chair.jpg "Low Res Haptic Display")

### Low-Res Haptic Display Side View 
![alt text](https://github.com/bfakhri/lrhi/blob/master/images/array_side.png "Low Res Haptic Display")

