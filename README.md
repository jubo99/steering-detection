# steering-detection
This repo is an overview of approaches to detect steering angle using external optic sensors as part of my master's thesis.

## Sensors
- [ ] Interiuer-camera
- [x] External camera
- [ ] External LiDAR
- [ ] Combination

Overview of pros and cons of sensors can be seen in the [Sensor Evaluation](SensorEvaluationMindMap.pdf).

### External camera
Currently a view approaches using an external camera in combination with OpenCV and [YoloV8](https://github.com/ultralytics/ultralytics.git) are being invastigated.

### OpenCV
In the [Repo](https://github.com/jubo99/steering-detection-frontal.git) template matching is being looked at. Template matching allows to search an image for a certain template (e.g. buttons on steering, markings).
