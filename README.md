# Inter-IIT-ISRO-2023-MID-PREP

### Google Drive Link to work on: https://drive.google.com/drive/folders/11FiTwiMUyVE1lkbSG6gU9WpdbcG7EVpS?usp=share_link

###DATASET LINK:
OHRC datas downloaded:https://drive.google.com/drive/folders/1W5D474XQA1pnF4KYgLzVVAgW2F2UcHEa?usp=sharing
TMC data downloaded : https://drive.google.com/drive/folders/1OEmK24mGoaSdu2dZx2hNBBBCgqNO00f9?usp=sharing

### Cropped OHRC train-test datatset : [Link](https://www.kaggle.com/datasets/arijitdas2002/tudumm) 

As we know that the problem statement is regarding enchancement of low resolution images(TMC dataset) to higher resolution, we used **SRResnet model**.

The srresnet.py file contains the code for the model of 21 layer deep network which we have used to train the images i.e from Low resolution to High Resolution images. We have trained the images and saved the weights of the model .


#### Overlap_calculator.ipynb

This code will help you to find the common parts of OHRC and TMC2 images and then cut out the largest rectangle which could be used for our training where the TMC2 part will be our input variable to our model and OHRC part will be our target variable to our model

#### SRResNet_training.ipynb

MSE-based SRResNet network is trained as initialization for the generator when training the actual GAN to avoid undesired local optima. we will be using this model for upscalling our images.

## Installation :

We used ***PDS4 Viewer*** software for viewing large xml files. Following is the installation code in python for the same:

``` !pip install pds4_tools```

After finding the overlapping patch in TMC and OHRC images, we need to get the rectangular image of maximum area, for that we used **MaxRect** library. Following is the installation code :

```https://pypi.org/project/maxrect/```

``` pip install git+https://${GITHUB_TOKEN}@github.com/planetlabs/maxrect.git```

We used the ***Spectral Angle Mapper*** as metric for validating our model. We imported that metric from **TorchMetrics**, the installation code is :

```
!pip install torchmetrics 
from torchmetrics import SpectralAngleMapper 
```

## Stacks Used :
1). pds4_tools [Link](https://pypi.org/project/pds4-tools/)

2). skimage [Link](https://scikit-image.org/)

3). torchmetrics [Link](https://pypi.org/project/torchmetrics/)

4). glob [Link](https://github.com/python/cpython/blob/3.11/Lib/glob.py)

5). tqdm [Link](https://tqdm.github.io/)

6). PIL [Link](https://pypi.org/project/Pillow/)

