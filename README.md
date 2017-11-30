# Pose Guided Person Image Generation (NIPS 2017)

This is an unofficial implementation.




# Descriptions of source files

config.py: parameters used for our network

dataset_reader.py: load training image data batches and process them for training

model_all.py: build G1, G2 & D in TensorFlow

network.py: helper class for building complicated networks

read_keypoint.py: adopt keras realtime multi-person pose estimation model to produce heatmap of human poses

trainall.py: the main training procedure

demo.py: use the pre-trained model to demo our result

dataset/: the directory which contain a small subset of the DeepFashion dataset. The full dataset is too large to submit, and we've signed an use agreement with the DeepFashion team so we did not upload all of the data.

System tested: Linux (Ubuntu)

# install pip3
sudo apt-get install python3-pip python3-dev

# install all required libraries
pip3 install -r requirements.txt

# use pre-trained model
Download model.tar.gz from https://drive.google.com/file/d/1z0mtWRSy_ObQ5NfXwXwcT9mIipIPxBsY/view?usp=sharing to project folder
Run command: tar -xvzf model.tar.gz
Run command: rm -rf logs
Run command: mv model logs
Run command: python3 demo.py
# train from scratch

Run command: rm -rf logs
Run command: python3 trainall.py

