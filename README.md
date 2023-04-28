# Comparison of Mask RCNN and Yolov8

### Task consition:

1. Take photos of your environment of two or more objects. (at least 100 instances between all objects) 

2. Annotate them on Roboflow for segmentation. 

3. Train a Mask RCNN model using detectron2

4. Train Yolov8  the smallest size for segmentation

5. Evaluate both models based on mAP and speed and size.

# Colab notebook 

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1s1MwHZnrsfIw4J7d0dkfHNrv9X_x9RDz?usp=sharing)

# Take photos of the environment

In this example, I have worked with objects such as a screwdriver and a wrench. Below are examples of data images of two types of objects:

<img src="https://github.com/rafailvv/mask-rcnn-vs-yolov8-aml/blob/main/examples/screwdriver.jpg" alt="Screwdriver" width="320"/><img src="https://github.com/rafailvv/mask-rcnn-vs-yolov8-aml/blob/main/examples/wrench.jpg" alt="Wrench" width="320"/>

# Annotation with roboflow

Next, I annotated 100 made objects (50 of each type) using roboflow

<img src="https://github.com/rafailvv/mask-rcnn-vs-yolov8-aml/blob/main/examples/annotation_screwdriver.jpg" alt="Annotation Screwdriver" width="1200"/>
<img src="https://github.com/rafailvv/mask-rcnn-vs-yolov8-aml/blob/main/examples/annotation_wrench.jpg" alt="Annotation Wrench" width="1200"/>
<img src="https://github.com/rafailvv/mask-rcnn-vs-yolov8-aml/blob/main/examples/annotation_dataset.jpg" alt="Annotation Dataset" width="1200"/>

# Mask RCNN using detectron2

Based on the official detectron2 and roboflow documentation, I was able to train RCNN using detectron2.

<img src="https://github.com/rafailvv/aml-faster-rcnn-vs-yolov8/blob/main/examples/rcnn_results.PNG" alt="RCNN Results" width="800"/>

# Yolov8

Based on the official documentation of yolo and rotoflow, I was able to train the Yolov8 model.

<img src="https://github.com/rafailvv/aml-faster-rcnn-vs-yolov8/blob/main/examples/yolo_results.png" alt="Yolov8 Results" width="800"/>
<img src="https://github.com/rafailvv/aml-faster-rcnn-vs-yolov8/blob/main/examples/yolo_results2.PNG" alt="Yolov8 Results 2" width="800"/>

# Comparison

**Mean Average Precision (mAP)**:
  - Faster RCNN: 84.53%
  - Yolov8: 93.33%

Yolov8 has slightly better mAP than RCNN.

**Speed:**
  - Faster RCNN: training for 1500 iterations in 56 minutes
  - Yolov8: training for 24 epochs in 2 minutes

Yolov8 is much faster than RCNN.

**Model size:**
  - Fater RCNN: 719.7 MB
  - Yolov8: 22.5 MB
  
Yolov8 is much smaller than RCNN.


**Thus, Yolov8 better in every way**

# Resources

- https://arxiv.org/abs/1506.01497
- https://github.com/pytorch/vision/blob/main/torchvision/models/detection/faster_rcnn.py
- https://github.com/tensorflow/models/tree/master/research/object_detection
- https://roboflow.com/
- https://blog.roboflow.com/faster-rcnn/
- https://arxiv.org/abs/2011.08036
- https://github.com/WongKinYiu/yolov8

