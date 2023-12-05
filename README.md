# Circular-Object-Counting

First we generated a sample dataset coded in notebook SIP_dataset_gen:
  It includes 3 options to generate the dataset: 1) circular objects with overlaping
                                                 2) circular objects without overlaping
                                                 3) circular objects with different shapes of gray based on radius without overlaping

![image_9](https://github.com/usmannanwarr/Circular-Object-Counting/assets/110171783/d3af7c31-8956-4f16-a7e4-393b03c2e9a6)

Next we annotated the objects using CVAT tool which made bounding boxes in format x_top_left, y_top_left, x_bottom_right, y_bottom_right however the format accepted by the YOLOv8 model is x_mid, y_mid, width, height so we transformed the format into YOLO accepted format in notebook Annotation Preprocessing

Finally we used YOLOv8 to predict bounding boxes for each image and counted them in notebook TrainYolov8CustomDataset
