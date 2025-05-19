
<div align="center">
<img src="https://github.com/17860421876/rxf1.github.io/blob/main/giajinde%20yolov8/RCEA.png" width="400px">
</div>

# RCEA-YOLOv8: A strawberry target precision detection method at different ripening stages under a novel attention mechanism

<div align="center">

  ![](https://img.shields.io/badge/python-3.8-red)
  [![](https://img.shields.io/badge/pytorch-2.0.0-red)](https://pytorch.org/)
  [![](https://img.shields.io/badge/torchvision-0.15.0-red)](https://pypi.org/project/torchvision/)
  
  
  

  [🛠️Installation Dependencies](https://blog.csdn.net/matt45m/article/details/134396179) |
  [🎤Introduction](https://github.com/ultralytics/ultralytics?tab=readme-ov-file) |
 
  [👀Download Dataset](https://pan.baidu.com/s/1WwJQXk5dpiTMP29icYjizQ )) |
  
  [🌊a Simple Anchor alignment metric](https://github.com/0811yu/0811yu.github.io) |
  [🚀Small Object detection improved](https://github.com/0811yu/0811yu.github.io) |
  
  [🤔Model generalization ability improved](https://github.com/0811yu/0811yu.github.io) |
 

</div>

## Dependencies:

 - Python 3.8
 - [PyTorch](https://pytorch.org/) 2.0
 - [Torchvision](https://pypi.org/project/torchvision/) 0.15.0
 - Ubuntu 20.04.5 LTS 
 - NVIDIA Tesla P100
   

## Introduction

The growth environment of strawberries is complex, and the morphology and structure are diversified. How to realize the accurate detection of strawberry targets in different maturity stages in complex scenarios is one of the main challenges facing the fine management and picking of strawberries. In this study, a novel RCEA-YOLOv8 model for strawberry target detection at different ripening stages. First, the RFCAConv (Receptive Field Coordinate Attention Convolutional) convolution mechanism is constructed in the backbone network to solve the problem of convolution kernel parameter sharing. Meanwhile, the C2f-SCConv coupling model was constructed to effectively utilize the SRU and CRU unit functions in SCConv to solve the problem of spatial and channel redundancy. Secondly, the neck network can retain channel information and reduces computational overhead, reshaping some channels into batch dimensions, and grouping channels into multiple sub-features, making spatial semantic features evenly distributed, so as to better extract image features. Finally, the data enhancement technology (Albu) is used to further improve the detection performance of the model in complex scenarios.

<div align="center">
<img src="https://github.com/17860421876/rxf1.github.io/blob/main/giajinde%20yolov8/RCEA-YOLOv8.png" width="700px">
</div>

## Ours Strawberries dataset
We have our largest strawberry data set, a total of 5600 photos, and use the data set expansion method (https://roboflow.com/) to expand the data set to 16800 images. The training, validation and test sets contained 10800,3000 and 3000 images, respectively. Dataset is named SID.

### SID Dataset example

<div align="center">
<img src="https://s2.loli.net/2023/09/06/r2G9ODnwQ8aomIx.jpg" width="450px">
</div>

</div>

## Result of experiment
The experiments conducted verified the contribution of the receptive field coordinate attention convolution mechanism (RFCAConv), C2f-SCConv coupling model, EMA attention mechanism and feature enhancement tool (Albu) to improve the performance of strawberry detection at different maturity stages.

### Ablation experiments in SID dataset
<div align="center">
  
<img src="https://github.com/17860421876/rxf1.github.io/blob/main/giajinde%20yolov8/Results%20of%20the%20ablation%20experiments.png" width="600px">

</div>

## The outcomes of our model tested on various datasets.
To assess the efficacy of the improved model on a variety of datasets, experiments were conducted on four different datasets for both the improved model and the baseline model. The following table presents diverse performance metrics, namely P, R, MAP50, MAP50-95 and Param(M), during training on the SID, StrawDI_Db1, and Internet datasets.

<div align="center">
<img src="https://github.com/17860421876/rxf1.github.io/blob/main/giajinde%20yolov8/3%20different%20strawberry%20datasets.png" width="600px">
</div>

 </div>
 
 ## Test result
a1 and a2 are the RCEA-YOLOv8 model test results, and b1 and b2 are the YOLOv8 model test results.

 <div align="center">
<img src="https://github.com/17860421876/rxf1.github.io/blob/main/giajinde%20yolov8/1.png" width="450px">
 </div>
