# Object-detection-using-YOLO-model

Things to remember:
* YOLO is a state-of-the-art object detection model that is fast and accurate
* It runs an input image through a CNN which outputs a 19x19x5x85 dimensional volume.
* The encoding can be seen as a grid where each of the 19x19 cells contains information about 5 boxes.
* Filter through all the boxes using non-max suppression. Specifically:
    * Score thresholding on the probability of detecting a class to keep only accurate (high probability) boxes
    * Intersection over Union (IoU) thresholding to eliminate overlapping boxes
* Because training a YOLO model from randomly initialized weights is non-trivial and requires a large dataset as well as lot of computation, we used previously trained model parameters in this exercise. If you wish, you can also try fine-tuning the YOLO model with your own dataset, though this would be a fairly non-trivial exercise.

References: 

The ideas presented in this notebook came primarily from the two YOLO papers. The implementation here also took significant inspiration and used many components from Allan Zelener's GitHub repository. The pre-trained weights used in this exercise came from the official YOLO website.
Joseph Redmon, Santosh Divvala, Ross Girshick, Ali Farhadi - You Only Look Once: Unified, Real-Time Object Detection (2015)
Joseph Redmon, Ali Farhadi - YOLO9000: Better, Faster, Stronger (2016)
Allan Zelener - YAD2K: Yet Another Darknet 2 Keras
The official YOLO website (https://pjreddie.com/darknet/yolo/)

Car detection dataset: 

Sample images taken from the Drive.ai Sample Dataset (provided by drive.ai) is licensed under a Creative Commons Attribution 4.0 International License(https://creativecommons.org/licenses/by/4.0/)
