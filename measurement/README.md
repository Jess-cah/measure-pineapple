# Measurement

* Jupyter notebooks `predict_measure_diameterLength.ipynb` and `predict_measure_projectedArea.ipynb` are used to extract pineapple fruit sizes from images. The Mask R-CNN pineapple detector trained in the [`detector`](https://github.com/Jess-cah/measure-pineapple/tree/main/detector) folder is used to locate pineapples in images. 
* In `predict_measure_diameterLength.ipynb`, the length and diameter of each detected fruit are extracted from the binary mask output using [OpenCV](https://opencv.org/). This involves, first, finding the polygon contour of the binary mask. Secondly, a minimum area bounding box is drawn around the mask polygon. The dimensions of the rotated bounding box are an approximation of the size of the fruit.
* In `predict_measure_projectedArea.ipynb`, the projected area of each detected mask is found.
