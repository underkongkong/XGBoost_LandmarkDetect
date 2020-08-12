# XGBoost_LandmarkDetect
This project uses the XGBoost model to realize face detection and landmarks detection without using the XGBoost package or sklearn package.
There are 3 classes in XGBoost model: "Node"/"Tree"/"Forest" 

# Dataset
The human faces pictures are selected from FDDB and xxx.

# Feature extract
HOG features is used for both face detecting and landmarks regression. 

# Face detection
The Face-detect dataset concludes 1000 positive samples and 1000 negative samples for human faces detecting. Each picture has a HOG feature vector and a label. XGBoost can select the best split points after train process. The value of a picture predicted by the model decide whether it is a human face picture.

# Landmarks detection
Labels of a picture are the position of 12 keypoints. There are two method for landmarks detection:
  1.To regress 12 keypoints in one forest
  2.To regress 1 keypoint in a forest, build 24(12x2) forests
 Both can achieve good results.
