# RoadDamageDetector

## News
Road damage detection and classification challenge (one of the IEEE Bigdata Cup Challenge) is underway. Please confirm [here](https://bdc2018.mycityreport.net/)! The registration is up to June 11.

## Citation
If you use or find out our dataset useful, please cite [our paper](https://arxiv.org/abs/1801.09454):

**arXiv:1801.09454 [cs.CV]**

@misc{1801.09454,
Author = {Hiroya Maeda and Yoshihide Sekimoto and Toshikazu Seto and Takehiro Kashiyama and Hiroshi Omata},
Title = {Road Damage Detection Using Deep Neural Networks with Images Captured Through a Smartphone},
Year = {2018},
Eprint = {arXiv:1801.09454},
}


## Abstract

Research on damage detection of road surfaces using image processing techniques has been actively conducted achieving considerably high detection accuracies.
However, many studies only focus on the detection of the presence or absence of damage. However, in a real-world scenario, when the road managers from a governing body needs to repair such damage, they need to know the type of damage clearly to take effective action. In addition, in many of these previous studies, the researchers acquire their own data using different methods. Hence, there is no uniform road damage dataset available openly, leading to the absence of a benchmark for road damage detection.
This study makes three contributions to address these issues.
First, to the best of our knowledge, for the first time, a large-scale road damage dataset is prepared. This dataset is composed of 9,053 road damage images captured with a smartphone installed on a car, with 15,435 instances of road surface damage included in these road images. These images are captured in a wide variety of weather and illuminance conditions. In each image, the bounding box representing the location of the damage and the type of damage are annotated.
Next, we use the state-of-the-art object detection method using convolutional neural networks to train the damage detection model with our dataset, and compare the accuracy and runtime speed on both, a GPU server and a smartphone. Finally, we show that the type of damage can be classified into eight types with high accuracy by applying the proposed object detection method.
The road damage dataset, our experimental results, and the developed smartphone application used in this study are made publicly available.
This page introduces the road damage dataset we created.


# Road Damage Dataset
## The structure of Road Damage Dataset
Road Damage Dataset contains trained models and Annotated images.
Annotated images are presented as the same format to [PASCAL VOC](http://host.robots.ox.ac.uk/pascal/VOC/).
- trainedModels
    - SSD Inception V2
    - SSD MobileNet
- RoadDamageDataset (dataset structure is the same format as PASCAL VOC)
    - Adachi
        - JPEGImages : contains images
        - Annotations : contains xml files of annotation
        - ImageSets : contains text files that show training or evaluation image list
    - Chiba
    - Muroran
    - Ichihara
    - Sumida
    - Nagakute
    - Numazu

## Download Road Damage Dataset
Please pay attention to the disk capacity when downloading.
- [trainedModels (70MB)](https://s3-ap-northeast-1.amazonaws.com/mycityreport/trainedModels.tar.gz)
- [RoadDamageDataset (1.7GB)](https://s3-ap-northeast-1.amazonaws.com/mycityreport/RoadDamageDataset.tar.gz)

## Dataset Tutorial
We also created the tutorial of Road Damage Dataset.
In this tutorial, we will show you:
- How to download Road Crack Dataset
- The structure of the Dataset
- The statistical information of the dataset
- How to use trained models.

Please check [RoadDamageDatasetTutorial.ipynb](https://github.com/sekilab/RoadDamageDetector/blob/master/RoadDamageDatasetTutorial.ipynb).

## Smartphone Apps
We also make our smartphone apps publicly available.
Please check [here](https://github.com/sekilab/RoadDamageDetector/blob/master/smartphoneAPPS.md).

## Privacy matters
Our dataset is openly accessible by the public. Therefore, considering issues with privacy, based on visual inspection, when a person's face or a car license plate are clearly reflected in the image, they are blurred out.


## License
Images on this dataset are available under the [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0). The license and link to the legal document can be found next to every image on the service in the image information panel and contains the CC BY-SA 4.0 mark:
<br><a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/deed.en"><img alt="Creative Commons License" style="border-width:0" src="https://licensebuttons.net/l/by-sa/4.0/88x31.png" /></a><br />


If you have something to ask us about the dataset, please contact :
`maedahi[at]iis.u-tokyo.ac.jp`
