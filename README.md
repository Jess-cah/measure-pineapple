# Object Detection and Size Determination of Pineapple Fruit at a Juicing Factory

The aim of this research was to develop a method for determining pineapple fruit size from images. This was achieved by first detecting pineapples in each image using Mask Region-based Convolutional Neural Network (Mask R-CNN) and then extracting the pixel diameter and length measurements, and the projected areas, from the detected mask outputs using OpenCV.

![Method_breakdown](sample_images/SizeDetProcess.png)

The repository includes:
* Datasets
* Colab notebook for training Mask R-CNN models for pineapple detection
* Jupyter notebook for size extraction from detected masks using OpenCV
