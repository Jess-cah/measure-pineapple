# Object Detection and Size Determination of Pineapple Fruit at a Juicing Factory

The aim of this research was to develop a method for determining pineapple fruit size from images. This was achieved by first detecting pineapples in each image using the [matterport implementation](https://github.com/matterport/Mask_RCNN) of Mask Region-based Convolutional Neural Network ([Mask R-CNN](https://arxiv.org/abs/1703.06870)) and then extracting the pixel diameter and length measurements, and the projected areas, from the detected mask outputs using OpenCV.

In the image below, (A) shows the masks detected by a Mask R-CNN trained to locate pineapples on a conveyor belt, (B) shows one of the binary mask outputs of the Mask R-CNN and (C) shows the rotated minimum area bounding box enclosing the binary mask.
![Method_breakdown](sample_images/sizeDetProcess.png)

The repository includes:
* Datasets for:
    - Training, validation and testing of Mask R-CNN
    - Evaluation of size determination approach
* Colab notebook for training Mask R-CNN models for pineapple detection
* Jupyter notebook for size extraction from detected masks using OpenCV
