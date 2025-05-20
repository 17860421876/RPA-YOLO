
<div align="center">
<img src="https://github.com/17860421876/RPA-YOLO/blob/main/RPA-YOLO/RPA.png" width="400px">
</div>

# An end-to-end pedestrian detection algorithm based on an adaptive multi-scale multi-branch receptive field attention mechanism

<div align="center">

  ![](https://img.shields.io/badge/python-3.9-red)
  [![](https://img.shields.io/badge/pytorch-2.0.1-red)](https://pytorch.org/)
  [![](https://img.shields.io/badge/torchvision-0.15.2-red)](https://pypi.org/project/torchvision/)
  
  
  

  [🛠️Installation Dependencies](https://blog.csdn.net/matt45m/article/details/134396179) |
  [🎤Introduction](https://github.com/ultralytics/ultralytics?tab=readme-ov-file) |
  [🌊a Simple Anchor alignment metric](https://github.com/0811yu/0811yu.github.io) |
  [🚀Small Object detection improved](https://github.com/0811yu/0811yu.github.io) |
  
  [🤔Model generalization ability improved](https://github.com/0811yu/0811yu.github.io) |
 

</div>

## Dependencies:

 - Python 3.9.20
 - [PyTorch](https://pytorch.org/) 2.0.1
 - [Torchvision](https://pypi.org/project/torchvision/) 0.15.2
 - Ubuntu 20.04.5 LTS 
 - NVIDIA GeForce RTX 3090
   

## Introduction

This study proposes a novel RPA-YOLOv10 detection architecture, aiming to achieve precise detection of pedestrian targets in different directions and distances within complex scenes by integrating an efficient attention mechanism. Firstly, an efficient multi-scale receptive field attention convolution mechanism is incorporated into the backbone network, effectively alleviating the limitation of shared convolution kernel parameters. By reconfiguring some channels to the batch dimension and grouping sub-features, the channel information is retained and the spatial semantic features are evenly distributed, thereby reducing computational costs. Subsequently, a multi-path feature extraction module is further designed and coupled with the C2f module, combining some multi-scale convolutions and diversified feature paths, effectively enriching feature representation and enhancing the perception ability for multi-scale targets. Finally, the AFGCA attention mechanism is integrated into the neck network, modeling the relationship between global and local information at multiple granularity levels through the correlation matrix, further improving the consistency and sharpening ability of feature fusion.

<div align="center">
<img src="https://github.com/17860421876/RPA-YOLO/blob/main/RPA-YOLO/RPA-YOLOV10.png" width="700px">
</div>

## Ours Strawberries dataset
We have our largest strawberry data set, a total of 5600 photos, and use the data set expansion method (https://roboflow.com/) to expand the data set to 16800 images. The training, validation and test sets contained 10800,3000 and 3000 images, respectively. Dataset is named SID.

### SID Dataset example

<div align="center">
<img src="https://github.com/17860421876/RPA-YOLO/blob/main/RPA-YOLO/xingrenzhaopian.png" width="450px">
</div>

</div>

## Result of experiment
The experiments conducted verified the contribution of the receptive field coordinate attention convolution mechanism (RFCAConv), C2f-SCConv coupling model, EMA attention mechanism and feature enhancement tool (Albu) to improve the performance of strawberry detection at different maturity stages.

### Ablation experiments in SID dataset
<div align="center">
  
<img src="https://github.com/17860421876/RPA-YOLO/blob/main/RPA-YOLO/Results%20of%20the%20ablation%20experiments.png" width="600px">

</div>

## The outcomes of our model tested on various datasets.
To assess the efficacy of the improved model on a variety of datasets, experiments were conducted on four different datasets for both the improved model and the baseline model. The following table presents diverse performance metrics, namely P, R, MAP50, MAP50-95 and Param(M), during training on the SID, StrawDI_Db1, and Internet datasets.

<div align="center">
<img src="https://github.com/17860421876/RPA-YOLO/blob/main/RPA-YOLO/Three%20different%20pedestrian%20datasets.png" width="600px">
</div>

 </div>
 
 ## Test result
a1 and a2 are the RCEA-YOLOv8 model test results, and b1 and b2 are the YOLOv8 model test results.

 <div align="center">
<img src="https://github.com/17860421876/RPA-YOLO/blob/main/RPA-YOLO/Results%20of%20the%20ablation%20experiment.png" width="450px">
 </div>
