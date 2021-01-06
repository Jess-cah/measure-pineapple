# Detector

## Training
* Colab notebook `maskpine_160images_coco_resnet50_aug4_ALL_01.ipynb` shows training of Mask R-CNN using COCO starting weights and ResNet50 backbone, and employing data augmentation techniques. Colab was used in order to make use of GPU facilities.
* Use `init_with = "coco"` to initialise with MS COCO starting weights. Can also use `"imagenet"` to initialise with ImageNet starting weights.
* In `pineapple.py`, `BACKBONE = "resnet50"` means that a ResNet50 CNN backbone will be used. Alternatively, this can be set to `"resnet101"`.
* Try other augmentation strategies by updating `aug`. For example:

**Data augmentation**
1. Gaussian noise and gaussian blurring
```
# define augmenter
aug = iaa.OneOf([iaa.Noop(),
                 iaa.Add((50)),
                 iaa.Add((-50))
                ])

# Noop is an alias for Identity (image left unchanged)
# i.e. each image will either be (A) left as is (B) Blurred or (C) have noise added
# there is a 33.3% chance of each occuring
```

2. Horizontal flipping
```
# define augmenter
aug = imgaug.augmenters.Fliplr(0.5)

# In this case, there is a 50% chance of an image being horizontally flipped
```

## Evaluation
* Detectors are evaluated using AP@0.5 and AP@[0.50:0.05:0.95], as shown in `maskpine_inspect_model.ipynb`.
