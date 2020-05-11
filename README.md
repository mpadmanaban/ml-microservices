[![CircleCI](https://circleci.com/gh/mpadmanaban/ml-microservices.svg?style=svg)](https://circleci.com/gh/mpadmanaban/ml-microservices)

## Project Summary

Project goal is to operationalize a a Machine Learning Microservice API using Kubernetes, which is an open-source system for automating the management of containerized applications. 
We have a pre-trained 'sklearn' model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. Here is [the data source site](https://www.kaggle.com/c/boston-housing)

---

## Setup the Environment

* Create a virtualenv and activate it
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

To test the app, Run: `./run_prediction.sh` after running the app.

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl


## Files in this project (in alphabetical order)
* `.circleci/config.yaml`:  Config file for CircleCI builds.
* `model_data`: Pre-trained 'sklearn' model that has been trained to predict housing prices in Boston.
* `output_txt_files`: Output from the app after running a predictaion.
* `Dockerfile`: Docker definition, Contains all the commands to assemble the image for Docker
* `Makefile`: Contains a set of directives used to build software.
* `app.py`:  Our microservice web python app.
* `make_prediction.sh`: tets script to send input to app and get results.
* `requirements.txt`: List of dependencies to install for our app.
* `run_docker.sh`: Script that runs our app in a Docker container.
* `run_kubernetes.sh`: Script that runs our app in Kubernetes.
* `upload_docker.sh`: Script that tags and commits our app Docker image to DockerHub repository.
