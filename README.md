# YOLO

## Reference

- [YOLO clarification](https://pysource.com/2019/06/27/yolo-object-detection-using-opencv-with-python/)

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

<b>Performance Metrics</b>

<img src="/img/iou.png" height="150" width="200"> <img src="/img/performance_metrics.jpg" height="150" width="500">

- [객체 커스텀](https://velog.io/@kjyggg/Few-Shot-Object-Detection)

- [커스텀 모델](https://blog.mutti.kr/m/160)
정확도를 높이는 방법
클래스당 2000개 이상의 이미지가 필요합니다.
이미지 속 객체들의 크기, 밝기, 위치, 회전, 배경이 다양할 수록 정확도가 높아집니다.
검출하지 않으려는 객체들의 사진도 필요합니다. (이 사진들은 빈 txt 파일을 가져야 합니다.)
roi 파일이 없는 이미지들의 roi를 파일을 만들어 주는 파이썬 코드를 첨부합니다.
