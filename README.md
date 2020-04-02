# <center>Real Time Object Detection and Segmentation using Mask R-CNN</center>

<figure>
<center>
<img src='https://raw.githubusercontent.com/matterport/Mask_RCNN/master/assets/4k_video.gif' />
<figcaption>Scene Understanding in real time</figcaption></center>
</figure>

Mask RCNN is a deep neural network aimed to solve instance segmentation problem in machine learning or computer vision. In other words, it can separate different objects in an image or a video. You give it an image, it gives you the object bounding boxes, classes and masks.


<br>


There are two stages of Mask RCNN. First, it generates proposals about the regions where there might be an object based on the input image. Second, it predicts the class of the object, refines the bounding box and generates a mask in pixel level of the object based on the first stage proposal. Both stages are connected to the backbone structure. What is backbone? Backbone is a FPN style deep neural network. It consists of a bottom-up pathway , a top-bottom pathway and lateral connections. Bottom-up pathway can be any ConvNet, usually ResNet or VGG, which extracts features from raw images. Top-bottom pathway generates feature pyramid map which is similar in size to bottom-up pathway. Lateral connections are convolution and adding operations between two corresponding levels of the two pathways. FPN outperforms other single ConvNets mainly for the reason that it maintains strong semantically features at various resolution scales.


## Scene Understanding

<br>

* **Object Localisation** - The task of object localization is to predict the object in an image as well as its boundaries. The difference between object localization and object detection is subtle. Simply, object localization aims to locate the main (or most visible) object in an image while object detection tries to find out all the objects and their boundaries.

* **Object Detection** - Object detection is a computer vision technique for locating instances of objects in images or videos. Object detection algorithms typically leverage machine learning or deep learning to produce meaningful results. When humans look at images or video, we can recognize and locate objects of interest within a matter of moments. The goal of object detection is to replicate this intelligence using a computer.

* **Image Segmentation** - Image segmentation is the process of partitioning a digital image into multiple segments that share similar attributes(like color, ) to simplify the representation and making it more useful for the analysis and interpretations. 


<figure>
<center>
<img src='https://miro.medium.com/max/760/1*Mj8WKVKf_RpiAsX3SC1ZdQ.png' />
</center>
</figure>



Object detection can be done via different SOTA algorithms:

1. R-CNN
2. Faster R-CNN
3. SSD(Single Short Detector)
4. YOLO (You Only Look Once)
5. Feature Pyramid networks
6. RetinaNet (Focal loss)
