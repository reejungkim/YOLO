# YOLO

## Reference

-[YOLO clarification](https://pysource.com/2019/06/27/yolo-object-detection-using-opencv-with-python/)

deep learning framework to run YOLO algorythm

1. Darknet : it’s the framework built from the developer of YOLO and made specifically for yolo.
   Advantage: it’s fast, it can work with GPU or CPU
   Disadvantage: it olny works with Linux os
2. Darkflow: it’s the adaptation of darknet to Tensorflow (another deep leanring framework).
   Advantage: it’s fast, it can work with GPU or CPU, and it’s also compatible with Linux, Windows and Mac.
   Disadvantage: the installation it’s really complex, especially on windows
3. Opencv: also opencv has a deep learning framework that works with YOLO. Just make sure you have opencv 3.4.2 at least.
   Advantage: it works without needing to install anything except opencv.
   Disadvantage: it only works with CPU, so you can’t get really high speed to process videos in real time.

<b>weight file</b>: trained model.
<b>cfg file</b>: configuration file where settings of the algorythm are presented
<b>name files</b>: name of the objets that the alorythm can detect.

YOLO accepts three sizes of image:
Blob is used to extract features fromt he iamge and to resize them.
320×320 it’s small so less accuracy but better speed
609×609 it’s bigger so high accuracy and slow speed
416×416 it’s in the middle and you get a bit of both.
