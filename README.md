# Lacmus Android Application 

Find missing people in photos on your android device. 

![Lacmus application screen preview](doc/lacmus_app_preview.png)

## Installation

todo

## Usage

1. Click (+) button in the right bottom of screen to open images. 
2. Select images, where you want to detect peoples. 
3. Click open, and you will see grid of selected images on main screen of application. Objects detection algorithm starts in background automatically. 
4. Image frames have three colours: 
- ${\color{red}Red}$ - processed, found people. 
- ${\color{green}Green}$ - processed, not found people. 
- ${\color{gray}Gray}$ - processing in progress.
5. Click on image, and you can see it in the fullscreen, zoom and swap. 
6. To exit application just click back button few times. 

## Developer zone

We use recommended app [architecture](https://developer.android.com/topic/architecture#recommended-app-arch).  

![Application acrchitecture](doc/arch.jpg)

We use recommended model [EfficientDet-Lite0](https://www.tensorflow.org/lite/android/tutorials/object_detection).   

We use tflite model maker for finetune object detection model on custom lacmus dataset with [this](https://www.tensorflow.org/lite/models/modify/model_maker/object_detection) tutorial. 
Original lacmus high dimension images adopted to small model input: resized and crops to 3x4=12 items with 320x320 size.   

Crop and resize also applied to input images in the Lacmus Android application.  
