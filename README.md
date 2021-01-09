# Facial-landmark-detection

## Introduction
This is a tutorial for facial landmark detection, the training model is **HRNet** and the data set is **300W**.
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
1. You need to download 300-W image set and annotations from <https://ibug.doc.ic.ac.uk/resources/300-W/>
2. Create folder ```data``` in ``` HRNet-Facial-Landmark-Detection-master```  
Directory shold like this:
```
-- data
   |-- 300w
       |-- images
       |   |-- afw
       |   |-- helen
       |   |-- ibug
       |   |-- lfpw
       |   ...
       |-- face_landmarks_300w_test.csv
       |-- face_landmarks_300w_train.csv
       |-- face_landmarks_300w_valid.csv
       |-- face_landmarks_300w_valid_challenge.csv
       |-- face_landmarks_300w_valid_common.csv
```
## Train
Start training after adjusting the parameters
```
python tools/train.py --cfg experiments/300w/face_alignment_300w_hrnet_w18.yaml
```
## Training model and test results
1. The training model will be saved in ```output\300W\face_alignment_300w_hrnet_w18```
2. Test the optimal model and output the result
```
python tools/test.py --cfg experiments/300w/face_alignment_300w_hrnet_w18.yaml --model-file output\300W\face_alignment_300w_hrnet_w18\final_state.pth
```
