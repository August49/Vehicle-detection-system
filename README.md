# Yolo v3 Object Detection in Tensorflow

## Getting started

### Prerequisites

This project is written in Python 3.6.6 using Tensorflow (deep learning), NumPy (numerical computing), Pillow (image processing), OpenCV (computer vision) and seaborn (visualization) packages.

```
pip install -r requirements.txt
```

### Downloading official pretrained weights

Let's download official weights pretrained on COCO dataset.

```
wget -P weights https://pjreddie.com/media/files/yolov3.weights
```

### Save the weights in Tensorflow format

Save the weights using `load_weights.py` script.

```
python load_weights.py
```

## Running the model

Now you can run the model using `detect.py` script. Don't forget to set the IoU (Intersection over Union) and confidence thresholds.

### Usage

```
python detect.py <images/video> <iou threshold> <confidence threshold> <filenames>
```

### Images example

Let's run an example using sample images.

```
python detect.py images 0.5 0.5 data/images/dog.jpg data/images/bus.jpg
```

Then you can find the detections in the `detections` folder.
<br>

### Video example

You can also run the script with video files.

```
python detect.py video 0.5 0.5 data/video/carDriving.mp4
```

## Acknowledgments

This project is inspired by the following resources:

- [Tensorflow Object Detection API](https://github.com/tensorflow/models/tree/master/official/vision/detection)
- [Yolo v3 official website](https://pjreddie.com/darknet/yolo/)
- [Yolo v3 official paper](https://arxiv.org/abs/1804.02767)
- [A Tensorflow Slim implementation](https://github.com/mystic123/tensorflow-yolo-v3)
- [ResNet official implementation](https://github.com/tensorflow/models/tree/master/official/resnet)
- [DeviceHive video analysis repo](https://github.com/devicehive/devicehive-video-analysis)
- [VIZAG (4K) Car Driving @Worlds Most Beautiful Beach City, INDIA](https://www.youtube.com/watch?v=ZHL9aA3y-so)
