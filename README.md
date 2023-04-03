# Deploying Docker Containers with GitHub Actions and Ansible Playbook

![flow (1)](https://user-images.githubusercontent.com/91386217/229526138-77365754-9ab6-4578-9a6c-0f8db62e1fa9.jpg)

This document outlines the process of deploying a Docker container to a set of worker nodes using GitHub Actions and Ansible Playbook. The deployment process involves the following steps:

#### Pushing the code from the local repository to the GitHub repository.
#### Triggering the GitHub Actions pipeline. 
#### Checking for code quality and required files, building a Docker image from the Dockerfile, and uploading it to Docker Hub. Then copying the Ansible playbook from the repository to the MasterNode. 
#### Installing Docker and its required packages in the worker nodes using Ansible Playbook. Also installing Python. Then logging into Docker Hub and pulling the image and running the container.**

## Step 1: Pushing the code to GitHub
The first step is to push the code from the local repository to the GitHub repository. This can be done using the git push command.

## Step 2: Triggering the GitHub Actions pipeline
After the code is pushed to the GitHub repository, the GitHub Actions pipeline is triggered. The pipeline is defined in the .github/workflows directory of the repository. It consists of one or more jobs that are executed sequentially.

## Step 3: Building and uploading Docker image
The first job in the pipeline checks for code quality and required files. If the code quality is satisfactory and all required files are present, it builds a Docker image from the Dockerfile and uploads it to Docker Hub. This job also copies the Ansible playbook from the repository to the MasterNode.

## Step 4: Installing Docker and its dependencies using Ansible Playbook
The second job in the pipeline is to deploy the Docker container to the worker nodes. This job is executed using Ansible Playbook. The Ansible playbook installs Docker and its required packages in the worker nodes. It also installs Python. After that, it logs into Docker Hub and pulls the Docker image that was built in the previous job. Finally, it runs the Docker container.

Conclusion
This document has outlined the process of deploying a Docker container to a set of worker nodes using GitHub Actions and Ansible Playbook. By following these steps, you can easily automate the deployment of your Docker containers to your infrastructure.
