[![Yourfriendsudha](https://circleci.com/gh/Yourfriendsudha/DevopsML.svg?style=svg)](https://circleci.com/gh/Yourfriendsudha/DevopsML)

## Project Overview

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API. 

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

Your project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Test your project code using linting
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

**The final implementation of the project will showcase your abilities to operationalize production microservices.**

---
## Clone the Source code

git clone https://github.com/Yourfriendsudha/DevopsML.git
cd DevopsML/

## Setup the Environment

* Create a virtualenv and activate it
python3 -m venv ~/.devops
source ~/.devops/bin/activate

* Run `make install` to install the necessary dependencies


### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Upload to docker `./upload_docker.sh`
4. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally. use AWS cloud9 to have a preinstalled Docker setup
* Setup and Configure Kubernetes locally. 
* Create Flask app in Container
* Run via kubectl

## folder setup
1. .circleci folder contains the config file to run the automated test
2. modeldata folder contains application speciific data 
3. Multiple script files
   a. run_docker.sh - Build the docker image from the Dockerfile and Build the docker image from the Dockerfile;
   b. upload_docker.sh - push your docker image to the dockerpath
   c. run_kubernetes.sh - to configure and run local cluster 
   4. make_predictions.sh - responsible to send input data to your containerized flask application via the appropriate port and dispaly the output
   
4. output_txt_files
output_txt_files/docker_out.txt contains logs from the flask app
output_txt_files/kubernetes_out.txt containes logs and the prediction returned after running the app in Kubernetes

5. DockerFile - A file used to instruct to build the image

6. makefile - A file used to execute goals during application compilation that contains things like  install, all, uninstall, clean, lint, setup, etc,.

7. Requirements.txt -  to help install the dependencies easily




