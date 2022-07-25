[![CircleCI](https://circleci.com/gh/kenmusima/project-ml-microservice-kubernetes.svg?style=svg)](https://circleci.com/gh/kenmusima/project-ml-microservice-kubernetes)

## Project Overview

Operationalize a Machine Learning Microservice API. 

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests the ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Goals

The project is to operationalize a working machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. The project does the following:
* Test the code using linting
* Containerize an application using a Dockerfile.
* Deploy the containerized application using Docker and make a prediction.
* Showcase the log statements after running application.
* Uses Kubernetes to create a Kubernetes cluster.
* Deploys a container using Kubernetes and makes a prediction.

You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

**The final implementation of the project will showcase your abilities to operationalize production microservices.**

---

## Setup the Environment
* Install [minikube](https://minikube.sigs.k8s.io/docs/start/) for either Linix or Windows or Mac. A local kubernetes for learning and developing Kubernetes.
* Install [kubectl](https://kubernetes.io/docs/tasks/tools/) for either Linix or Windows or Mac. A cmd tool used for running cmds against Kubernetes clusters.
* Install [docker desktop](https://docs.python.org/3/library/venv.html) for either Linix or Windows or Mac. An application that is used to build and share containerized applications and microservices.
* Signup on (DockerHub)[https://hub.docker.com/] to publish image after successful build.
* Create a virtualenv with Python 3.7 and activate it. Refer to this link for help on specifying the Python version in the virtualenv.
```bash
python3 -m pip install --user virtualenv
# You should have Python 3.7 available in your host. 
# Check the Python path using `which python3`
# Use a command similar to this one:
python3 -m virtualenv --python=<path-to-Python3.7> .mlmicroserviceapp
source .mlmicroserviceapp/bin/activate
```
For Windows to create virtualenv follow this link [virtualenv](https://docs.python.org/3/library/venv.html)
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Docker Steps

* Setup and configure Docker using link above.
* Change tag and app name in `./run_docker.sh`.
* Run `./run_docker.sh`

### Publish to DockerHub
* Setup and configure Docker using link above.
* Setup a DockerHub account and create a Repository.
* Publish image. 

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl

### Useful Troubleshooting Commands and Links
Publishing [tutorial](https://docs.docker.com/docker-hub/)
```bash
# List the images built
docker image ls
# List all the pods including the status
kubectl get pods
# Check status of a pod by replacing podname with the actual name.
kubectl describe pod [podname]
```