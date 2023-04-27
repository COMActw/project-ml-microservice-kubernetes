[![CircleCI](https://dl.circleci.com/status-badge/img/gh/COMActw/project-ml-microservice-kubernetes/tree/master.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/COMActw/project-ml-microservice-kubernetes/tree/master)

# Operationalize a Machine Learning Microservice API

## Project Overview
  This project focuses on applying the acquired skills in operationalizing a Machine Learning Microservice API. It involves the utilization of a pre-trained Scikit-learn model that predicts housing prices in Boston based on various features such as average rooms in a home, data about highway access, teacher-to-pupil ratios, and more. The project utilizes data that was initially obtained from Kaggle, and more information can be found on the data source site. The primary objective of the project is to operationalize a Python Flask app, which is provided in the app.py file. The app serves predictions (inference) about housing prices via API calls. The project is not limited to this specific machine learning model and can be extended to other pre-trained models such as those for image recognition and data labeling.
## Getting Started
### Install Docker

 1. Update existing list of packages
    ```
      sudo apt update
    ```
 2. Install a few prerequisite packages which let apt use packages over HTTPS
    ```
      sudo apt install apt-transport-https ca-certificates curl software-properties-common
    ```
 3. Add the GPG key for the official Docker repository to your system
    ```
      curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
    ```
 4. Add the Docker repository to APT sources
    ```
      sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
    ```
 5. Make sure to install from the Docker repo
    ```
      apt-cache policy docker-ce
    ```
 6. Install Docker
    ```
      sudo apt install docker-ce
    ```
 7. Check that it’s running
    ```
      sudo systemctl status docker
    ```

### Lints checks
  Run lint `make lint`

### Install K8s & Minikube
 1. Install the latest minikube stable release on x86-64 Linux using binary download
    ```
      curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
      sudo install minikube-linux-amd64 /usr/local/bin/minikube
    ```
 2. Start cluster
    ```
      minikube start
    ```
 3. Download the latest K8s release with the command
    ```
      curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
    ```
 4. Install kubectl
    ```
      sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
    ```
 5. Test to ensure the version is up-to-date
    ```
      kubectl version --client --output=yaml
    ```

## Dockerfile

 1. Config Dockerfile
 2. Run Docker container
 3. Make prediction 
 3. Logging the docker_out.txt file

## Kubernetes

 1. Config K8s
 2. Deploy with K8s
 3. Logging the kubernetes_out.txt file

## CircleCI Integration
 Verify the repo via CircleCI and add the status badge on top of this README
