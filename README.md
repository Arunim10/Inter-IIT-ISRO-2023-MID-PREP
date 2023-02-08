# Inter-IIT-ISRO-2023-MID-PREP

### Cropped OHRC train-test datatset : [Link](https://www.kaggle.com/datasets/arijitdas2002/tudumm) 

As we know that the problem statement is regarding enchancement of low resolution images(TMC dataset) to higher resolution, we used **SRResnet model**.

The srresnet.py file contains the code for the model of 21 layer deep network which we have used to train the images i.e from Low resolution to High Resolution images. We have trained the images and saved the weights of the model .

## Installation :

We used ***PDS4 Viewer*** for viewing large xml files. Following is the installation code in python for the same:

``` !pip install pds4_tools```


## Stacks Used
1. pds4_tools
2. skimage
3. torchmetrics
4. glob
5. tqdm
6. PIL


Overlap calculator

This file uses the meta data given with the images to return overlapping pairs of tmc and ohrc image which can be 
used as input and lable for our model.The meta data contains latitude and longitude of every 100th element of the image.
These latitude and longitude represent the real senario of image om surface of moon. Now the boundary of each image 
using these latitude and longitude is determined which is used for calculating the overlaping region which can be any polygon.
But for the convenience we reduce the region into a rectangle which can we used for training because model takes rectangles as 
input!.The boundary of this rectangle is used to get the pixel and scan value of each boundary point which are used for 
slicing the whole image, 2 sets of these are determined one for tmc and other for ohrc image. Images are then formed using the 
sliced array which are then cropped/resized which ever is needed foo maiking them sutaible for training.
Each ohrc image is compared to each tmc image.

## Stacks used
1.Pandas
2.Shapely
3.Cvxpy
4.Maxrect

