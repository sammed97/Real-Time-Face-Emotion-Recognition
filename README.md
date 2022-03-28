# Live Class Monitoring System- Face Emotion Recognition
![image](https://user-images.githubusercontent.com/85985250/160456385-112d0d64-74cd-46a2-b116-7b9476fd31de.png)

## Project Introduction:
The Indian education landscape has been undergoing rapid changes for the past 10 years owing to the advancement of web-based learning services, specifically, eLearning platforms. 
Global E-learning is estimated to witness an 8X over the next 5 years to reach USD 2B in 2021. India is expected to grow with a CAGR of 44% crossing the 10M users mark in 2021. Although the market is growing on a rapid scale, there are major challenges associated with digital learning when compared with brick and mortar classrooms. One of many challenges is how to ensure quality learning for students. Digital platforms might overpower physical classrooms in terms of content quality but when it comes to understanding whether students are able to grasp the content in a live class scenario is yet an open-end challenge.
In a physical classroom during a lecturing teacher can see the faces and assess the emotion of the class and tune their lecture accordingly, whether he is going fast or slow. He can identify students who need special attention. Digital classrooms are conducted via video telephony software program (ex. Zoom) where it’s not possible for medium scale class (25-50) to see all students and access the mood. Because of this drawback, students are not focusing on content due to lack of surveillance. While digital platforms have limitations in terms of physical surveillance but it comes with the power of data and machines which can work for you. It provides data in the form of video, audio, and texts which can be analysed using deep learning algorithms. Deep learning backed system not only solves the surveillance issue, but it also removes the human bias from the system, and all information is no longer in the teacher’s brain rather translated in numbers that can be analysed and tracked. 

## Task to do:
Our target is to solve above-mentioned challenge by applying deep learning algorithms to live video data. The solution to this problem is by recognizing facial emotions. 

## Summary:
I get the dataset from kaggle, which is ‘fer-2013’. After understanding the data, I processed the images for training purpose. I chose MobileNet and Convolutional Neural Network (CNN) models to perform. After training I get to know that CNN was better performer than MobileNet. So I saved the CNN model and then build the Streamlit application using github repository and pipelines. Also after that I deployed the application on Heroku.

## Components & Approach-
### 1.	Dataset: - 
I used a dataset named FER-2013 from kaggle. The data consists of 48x48 pixel grayscale images of faces. The faces have been automatically registered so that the face is more or less centred and occupies about the same amount of space in each image.
The task is to categorize each face based on the emotion shown in the facial expression into one of seven categories (0=Angry, 1=Disgust, 2=Fear, 3=Happy, 4=Sad, 5=Surprise, 6=Neutral). The training set consists of 28,709 examples and the public test set consists of 3,589 examples.

### 2.	Understanding Dataset: - 
In our data we have 35,887 images of 7 type of emotions with 3 columns. We don’t have any null values in our dataset. We have 3 features named emotions, pixels and Usage.

### 3.	EDA: - 
Got insights from data like, we have total 7 emotion types then we have 3 features. Got to know emotion wise distribution of data. Then got the train-test ratio within the data.
### 4.	Data Pre-processing: - 
Converted images into numpy arrays and make output categorical. After that splits the data in the ratio of 80:20 for train and test/validation respectively. Applied data augmentation on images to generate more data. In our problem we take each batch and apply some series of random transformations (random rotation, resizing, shearing) to increase generalizability of the model.

### 5.	Model Selection: 
### a.	MobileNet - 
•	As the name applied, the MobileNet model is designed to be used in mobile applications, and it is Tensor Flow’s first mobile computer vision model.
•	MobileNet uses depth wise separable convolutions. It significantly reduces the number of parameters when compared to the network with regular convolutions with the same depth in the nets. This results in lightweight deep neural networks.
•	MobileNet is a class of CNN that was open-sourced by Google, and therefore, this gives us an excellent starting point for training our classifiers that are insanely small and insanely fast.
•	The speed and power consumption of the network is proportional to the number of MACs (Multiply-Accumulates) which is a measure of the number of fused Multiplication and Addition operations. 
### b.	Convolutional Neural Network (CNN) – 
•	In deep learning, a convolutional neural network (CNN/ConvNet) is a class of deep neural networks, most commonly applied to analyse visual imagery. Now when we think of a neural network we think about matrix multiplications but that is not the case with ConvNet. It uses a special technique called Convolution. Now in mathematics convolution is a mathematical operation on two functions that produces a third function that expresses how the shape of one is modified by the other.
•	The convolutional neural network, or CNN for short, is a specialized type of neural network model designed for working with two-dimensional image data, although they can be used with one-dimensional and three-dimensional data. Central to the convolutional neural network is the convolutional layer that gives the network its name. This layer performs an operation called a convolution.
•	Here I am using keras with tensorflow as back-end for building Neural Networks.
The layers to be added are:-
1. Convolution layer
2. Pooling layer
3. Batch normalization
4. Activation Layer
5. Dropout Layer
6. Flatten Layer
7. Dense layer

### 6.	Model Evaluation: - 
After evaluating the model I get to know that CNN model was better in all parameters than MobileNet. CNN got the training accuracy of 70% and testing accuracy on test data was 78%, So I saved the CNN model for further operations.
![image](https://user-images.githubusercontent.com/85985250/160458499-fd6b4cb3-1c70-4faf-93b8-898044d7597b.png)


### 7.	Streamlit & Heroku Deployment: - 
First I pushed all my work into my relevant github repository, then I created required pipelines in github and after that I created the application on Streamlit. After successful building app on Streamlit, I deployed it on Heroku (Cloud Platform).

Demo on streamlit - https://share.streamlit.io/sammed97/face_emotion_recognition/main/app.py

Deployment on Heroku - https://face-emotion-detection-dl.herokuapp.com/

[Note: Hit refresh 3-4 times if page is taking too much time to load or it shows applicaton error on Heroku platform.]

### 8. Conclusion
1. After understanding of problem statement, I get the dataset from kaggle which is FER 2013 in csv format.
2. After EDA, I prepared image data for model building.
3. I used two models, one is MobileNet and other is Convolutional Neural Network (i.e. CNN).
4. I choose the CNN model as it has high training and testing accuracy than MobileNet and also it shows on Loss & Accuracy curves that CNN is better than MobileNet.
5. I saved the model and used to predict facial emotions.
6. Since dataset has a very less number of images for 'disgust', it doesn’t trained well on this emotion and hardly predict it.
7. After that for Streamlit application, I created several files on my github repository like procfile, requirement, runtime, setup, package, etc.
8. Then using my github repository, I created Streamlit app for demo purpose.
9. Then I deployed this app on Heroku which is cloud application platform.

### 9. Future Scope
1. We can train more powerful and accurate models with high computational powers.
2. We can get more data, so we can train even better.
3. We can reduce slug size while deploying on Heroku, so that it can run faster.

# Thank You !
