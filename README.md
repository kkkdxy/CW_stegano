# CW_stegano
[![PyPI](https://img.shields.io/pypi/v/nine.svg?maxAge=2592000)](https://pypi.python.org/pypi?:action=display&name=CW_stegano&version=1.0.0)    
A fun little python script that encodes and decodes strings and images    

(derived from steganography)

## Installation
### Windows
```batch
py -m pip install CW_stegano
```
### Linux
```Shell
sudo pip3 install CW_stegano
```
# Usage
### Encoding
This is easiest with an **example**:
```Python
import steganography as steg

img = steg.text_image("hello world.")
# read steg.text_image.__doc__ for more info.
# Note : this will also print a bunch of status updates and info on the computation

quiet_img = steg.text_image("When this image is created, there will be no printing",print_status=False)
# since print_status is set to false, the function will 
# not do all of its regular prints. (the default of print_status is True)

img.show()
# this is really more of a PIL function,
# but it's relevant that you should see the image that's created.
```
### Decoding
The most important part of this, is that the input for the function is a PIL.Image object **generated by steganography.text_image()**
```Python
import steganography as steg
img = steg.text_image("decode me!")

text = steg.decode_image(img)
print(text)
```
