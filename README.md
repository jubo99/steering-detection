# steering-detection
This repo is an overview of approaches to detect steering angle using external optic sensors as part of my master's thesis.

## Sensors
- [ ] Interiuer-camera
- [x] External camera
- [ ] External LiDAR
- [ ] Combination

Overview of pros and cons of sensors can be seen in the [Sensor Evaluation](SensorEvaluationMindMap.pdf).

## External camera
Currently a view approaches using an external camera in combination with OpenCV and [YoloV8](https://github.com/ultralytics/ultralytics.git) are being invastigated.

### OpenCV
In the [Repo](https://github.com/jubo99/steering-detection-frontal.git) template matching is being looked at. Template matching allows to search an image for a certain template (e.g. buttons on steering, markings).

![Template matched on image](TemplateMatching/template_match1.png)

### Yolo
The newest version of Yolo (You only look once) can also be used to detect steering (angle). Therefor, it got trained with custom data to perform detection and segmentation task on images of steering wheels.

**Detection**
- Trained on dataset with around 850 images
- Nano version of YoloV8 (smallest version)
- Weights in Yolov8_custom_weights folder

To run, execute following steps in Python3 environment:
1. Download weights
2. `pip install ultralytics`
3. `yolo predict model=detection_nano_wheel.pt source=PATH/TO/IMAGE`

*put image of results here*

**Segmentation**
- Trained with custom dataset with around 50 images (Very view images for training -> more images will most certainly increase quality dramaticly)
- Small version used for training (2nd smallest version)
- Weights in Yolov8_custom_weights folder

To run, execute following steps in Python3 environment:
1. Download weights
2. `pip install ultralytics`
3. `yolo segment predict model=best_segmentation_wheel.pt source=PATH/TO/IMAGE`

Results can be seen in the [Yolo_Segmenttation file](Yolo_Segmentation.pdf)

