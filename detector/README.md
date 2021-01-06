# Detector

* Colab notebook `maskpine_160images_coco_resnet50_aug4_ALL_01.ipynb` shows training of Mask R-CNN using COCO starting weights and ResNet50 backbone, and employing data augmentation techniques. Colab was used in order to make use of GPU facilities.
* Use `init_with = "coco"` to initialise with MS COCO starting weights. Can also use `"imagenet"` to initialise with ImageNet starting weights.
* In `pineapple.py`, `BACKBONE = "resnet50"` means that a ResNet50 CNN backbone will be used. Alternatively, this can be set to `"resnet101"`.
* Detectors are evaluated using AP@0.5 and AP@[0.50:0.05:0.95], as shown in `maskpine_inspect_model.ipynb`.
