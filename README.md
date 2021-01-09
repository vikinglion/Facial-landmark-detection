# Facial-landmark-detection

## Introduction

## Environment
* Windows10
* CUDA 10.2
* cuDNN v8.0.2
* GPU: NVIDIA GeForce GTX 1660 Ti

## Installation
1. Create a conda environment
```
conda create -n landmarkdetection python=3.8 -y
conda activate landmarkdetection
```
2. Install PyTorch 1.6.0+cu101
```
pip install torch==1.6.0 torchvision==0.7.0
```
3. Download HRNets at <https://github.com/HRNet/HRNet-Facial-Landmark-Detection>  
Or
```
git clone https://github.com/HRNet/HRNet-Facial-Landmark-Detection.git
```
4. Install build requirements
```
pip install -r requirements.txt
```
## Data
1. You need to download 300-W data set from <https://ibug.doc.ic.ac.uk/resources/300-W/>
