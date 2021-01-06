# Datasets

In the context of this work, there are two conveyor belts that transport fruit into the factory. A camera was installed over each conveyor belt, and these are known as Camera A and Camera B.

* Image datasets are saved as `datasets.zip` and can be accessed [here](https://drive.google.com/drive/folders/1OQQOM0r_9_lTYDCh-D4nksKNZFarVFyL?usp=sharing). 
* For the purpose of training and evaluating a Mask R-CNN pineapple detector, a total of 160 images of size 970 × 605 pixels were captured using Cameras A and B. These 160 images were randomly split into training, validation and test sets, ensuring that each set contained an equal number of images from Camera A and Camera B.
* For evaluation of the size determination approach, images were obtained of 120 pineapples that had previously been manually measured. As there are two conveyor belts delivering pineapples to the factory, 60 pineapples were placed on Conveyor A and 60 pineapples were placed on Conveyor B. 