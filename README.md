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
