# 3DHPE-RNN
3D Human Pose Estimation using RNNs



# Requirements

•	TensorFlow 1.0 or later

•	HDF5 for python

•	Python 3

•	OpenCV-python



# The repository contains 7 python files

•	cam.py: It loads the information of the cameras of Human3.6M dataset

•	data.py: It contains function for dealing with human3.6M dataset

•	model.py: It contains the model designed using RNNs with seq-to-seq network

•	procustes.py: It computes similarity transformation

•	skeleton.py: It contains functions to visualize human poses

•	train.py: It trains the model.

•	output.py: It generates a sequence of 3D poses from a sequence of 2D poses.



# Training the model from scratch

For training the model from scratch use the command:

Python train.py --use_sh –camera_frame –dropout 0.5



# Evaluating the trained model

To evaluate the trained model, use the command:

Python train.py –use_sh –camera_frame –dropout 0.5 –load 1798200 –evaluate 

Here, 1798200 is passed to load which is the checkpoint point for the global iteration number.



# Fine-tuning an existing model

Command:

Python train.py –use_sh –camera_frame –dropout 0.5 –load 1798200



# Create 3D poses from a sequence of 2D poses

Command:

Python output.py –use_sh –camera_frame
