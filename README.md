# Simplified-Midterm-Project

Project Presentation Link : [https://youtu.be/Teiy19syXFE](https://youtu.be/Teiy19syXFE)


# Introduction :

This project demonstrates training, testing, deploying a SKLearn model on AWS Sagemaker and accessing the model anywhere using a web application client.

# Model and Data :

Model Source and files can be downloaded using this [link](https://storage.googleapis.com/aiec-s24/4-%20Training%20a%20Static%20Malware%20Detector.zip)

This code is from Lab 5.4 where we are provided with all training code and dataset(Labeled PE files). The model used in this lab is RandomForestClassifier. 

# Deployment :

The models from Lab 5.4 are dumped and imported using the Joblib library. 
Later an inference script is created which is going to be used on AWS Sagemaker endpoint to process the input(PE features) sent from the client application. 
All the dependencies are noted in requirements.txt where the sagemaker will detect and install the missing ones.
All these are zipped into a model.tar.gz file which is uploaded to an S3 bucket and used for deployment.
Later endpoint is created using the zip file.

# Client :

I have created a client web application using Streamlit in python. This is executed in Google Colab. 

Users can upload a .exe file into the application and the backend code will extract PE features from them and going to pack it into a JSON and push it to the endpoint for prediction. 
It records the response from endpoint and displays the classification of the exe file uploaded.

# File structure in repo:

Each step (training, deployment, and client) is placed in different folders for easy understanding, but remember I have trained all these codes in the same path without these folder classifications. For the training script use the downloaded data from the Lab 5.4 file link provided it has all the data needed.

***Thank You😊***
