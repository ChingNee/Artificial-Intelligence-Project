# HANDWRITTEN CHARACTER RECOGNITION USING CONVOLUTIONAL NEURAL NETWORK

## A. PROJECT SUMMARY

**Project Title:** Handwritten Character Recognition

**Team Members:** 
- Cecilia Chong Ching Nee (B031910390)
- Siew Chung Seng (B031910342)
- Vishan Menan A/L Balakrishnan (B031910018)
- Muhammad Putra Alif Bin Ismail (B031910115)

- [ ] **Objectives:**
- to develop a character recognition system
- to prepare dataset for model training of character recognition system
- to predict character accurately with handwritten character recognition system


##  B. ABSTRACT 

Learning how to write the alphabet is one of the first steps in your child's journey of learning. By ages four to five, children will start writing letters. Children will learn to write the alphabet in preschool and kindergarden, bu it may be beneficial to have your child practice writing letters at home. Therefore, nowadays, some of the parents buy a handwriting workbook and get their child to go through the exercise in it page by page. However, this method need a lot of paper to practice the characters. In addition, it is more difficult for children to judge whether the alphabet that written by them are correct or wrong. 

The best way to teach the children to write the alphabet is doing practice using AI technology. Children can use this handwritten character recognition system to check their understanding quickly. It is because this system can predict what is the character that write in the text field provided and display the result. If the result is correct, it means that the child able to write this letter and know how to write it properly. 

![Coding](https://github.com/CeciliaChongChingNee/Artificial-Intelligence-Project/blob/main/AI-Project-Documentation/poster-handwrting.jpg)

Figure 1 shows the alphabet that will be learnt by the child and we will use them in this system


## C.  DATASET
This project will be split into 3 parts, which are:
- Preprocessing : Here we will focus on preprocessing the data to allow for better training results
- Training : Here we will focus on the training of the model and the validation of training results
- Deployment : In this stage we will deploy the model by loading it and allow user to interact with it through GUI such as website

Our dataset for training are shown as below:
![image](https://user-images.githubusercontent.com/80866120/115016783-224cec80-9ee8-11eb-8147-88782634bd45.png)

Figure 2 shows sample of the data used for training the model

The dataset we'll be using contains 26 folders (A-Z) containing handwritten images in size 2828 pixels, each alphabet in the image is centre fitted to 2020 pixel box.

Each image is stored as Gray-level

Kernel CSVToImages contains script to convert .CSV file to actual images in .png format in structured folder.

The images are taken from NIST(https://www.nist.gov/srd/nist-special-database-19) and NMIST large dataset and few other sources which were then formatted as mentioned above.

Our goal is to train a CNN model that is capable of predicting/recognizing the inputted image of a character.


## D.   PROJECT STRUCTURE
The following directory is our structure of our project

    ├── dataset
    │ ├── A-Z handwritten characters.csv [372,450 entries]
    | └── images
    |   ├── A
    |   └── B
    |   └── C
    |   └── D
    |   └── E
    |   └── F
    |   └── G
    |   └── H
    |   └── I
    |   └── J
    |   └── K
    |   └── L
    |   └── M
    |   └── N
    |   └── o
    |   └── P
    |   └── Q
    |   └── R
    |   └── S
    |   └── T
    |   └── U
    |   └── V
    |   └── W
    |   └── X
    |   └── Y
    |   └── Z
    ├── model
    │ ├── best_model.h5
    ├── trainModelScript.py
    ├── generateCSVScript.py
    ├── testModelScript.py
    └── server.py
    28 directories, 6 files


## E   TRAINING THE HANDWRITTEN CHARACTER RECOGNITION MODEL
We are now ready to train our model using Keras, Tensorflow, and CNN.

First we shall perpare the training data, go ahead and run the following command to generate the csv

$python generateCSVScript.py

Next we shall train the model and generate the model
Go ahead and run the following command:

$python trainModelScript.py

Moving on, we shall test the model by using our own sample data

$python testModelScript.py

Lastly, we shall deploy the model with the following command

$python server.py

## F.  RESULT AND CONCLUSION

Handwritten character recognition on website hosted in real-time

You can then launch the recognition using the following command

$python server.py

![image](https://user-images.githubusercontent.com/80866120/115021984-4f50cd80-9eef-11eb-8508-841611ded592.png)
Figure 3 shows result of model training and validation

As shown in the figure above, we are able to get an accuracy of 97.5% on our model.

[![Figure4](https://img.youtube.com/vi/vT1xNDjoTv0/0.jpg)](https://www.youtube.com/watch?v=vT1xNDjoTv0 "Figure4")

Figure 4 shows result by using handwritten character recognition system

## G.   PROJECT PRESENTATION 

In this project, you will be able to create a Handwritten character recoginition system using Keras, TensorFlow and CNN. To create the model we collect image of handwritten character and preprocessed them into csv for training purpose. We fine-tuned the model and is able to obtained a classifier that is 97.5% accurate.

We then load this model on a server that allows user to draw a character and use it to predict/recognize what did the user wrote.

[![demo](https://img.youtube.com/vi/qIdv7Nh5d0Q&t=84s/0.jpg)](https://www.youtube.com/watch?v=qIdv7Nh5d0Q&t=84s "demo")


