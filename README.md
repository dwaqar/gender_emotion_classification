# Project Title: Gender and Emotion Recognition

### Done by: Dania Maryam Waqar

### Section: 2

### Class: ECE 5831

# Summary of Work

In this project, we aimed to perform both gender and emotion recognition simultaneously. In order to do this, both networks were trained independently first to create gender and emotion recogntion models. These models have been saved. They are referenced by the main `video_emotion_gender_demo.py` file in order to perform both classification tasks in real time. Contributions have been made as detailed below, but mainly consist of efforts to improve the current performance of the algorithm through multiple iterations by changing the type of parameters used (batch size, type of optimizer, and learning rates). These efforts have proven successful as they have aided in a 6.04% and 1.7% improvement for emotion and gender recognition accuracies from the original benchmark paper.

# This project consists of the following files:

a) `datasets`: This folder holds the datasets that can be downloaded and unzipped from this link: https://drive.google.com/file/d/1Jy5wemcf71tG-Rf72fxaeIuvw331Bk-d/view?usp=sharing

b) `trained_models`: This contains the models that have been trained. Both gender and emotion recognition models are stored here, and will be referenced when the main gender and emotion recognition file is run.

c) `src`: This contains all the source code for training the gender and emotion recognizers, for running them separately, and to run them together. The main project file is called `video_emotion_gender_demo.py`.

# To reproduce code:

In order to reproduce the code, the following steps must be done:

a) Download the dataset from the link above and save it as the ```datasets/``` folder.

b) Ensure the following dependencies have been installed in your environment:
  
  - h5py==3.7.0

  - keras==2.10.0

  - numpy==1.23.1

  - opencv-python==4.6.0

  - pandas==1.4.2

  - tensorflow==2.10.0

c) _From the `src/` folder_ run ```video_emotion_gender.py```

# Contributions to the original code:

a) Addition of the `video_gender_demo.py` file: The code to run gender recognition independently did not exist in the original code files. In order to test gender recognition, we created this file successfully and tested it out, as seen in the Figure below (Figures only visible on main Github page).

<img width="200" alt="Screen Shot 2022-12-12 at 11 29 50 AM" src="https://user-images.githubusercontent.com/120402562/207099888-46e3a71c-01d9-4d4f-af65-22a74e0a3a00.png"> <img width="200" alt="Screen Shot 2022-12-12 at 11 32 20 AM" src="https://user-images.githubusercontent.com/120402562/207100484-515389bc-06ff-42a9-b96b-dc42241a41f0.png">

b) The `train_emotion_classifier.py` file: This file has been modified in terms of its batch size (it is now 64), type of optimizer (it is now Nadam), and learning rate (it remains as 0.001). These modifications led to a 6.04% improvement in accuracy from the original paper, and a 0.65% improvement from our replicated training iteration.

c) The `train_gender_classifier.py` file: This file has been modified in terms of its batch size (it is now 64), type of optimizer (it is now Nadam), and learning rate (it remains as 0.001). These modifications led to a 1.7% improvement in accuracy from the original paper, and a 0.07% improvement from our replicated training iteration.

# Links

1. Link to dataset: https://drive.google.com/file/d/1Jy5wemcf71tG-Rf72fxaeIuvw331Bk-d/view?usp=sharing

2. Link to Project Presentation: https://youtu.be/rARmLUJ-fHY

3. Link to Project Demo: https://youtu.be/KldZt2SMbPc

4. Link to Project GitHub Code: https://github.com/dwaqar/gender_emotion_classification

# Credit
This work is based upon the work done by https://github.com/oarriaga/face_classification.
