# US-Visa-Approval-Prediction: End-to-End ML Model Deployment in AWS

## How to run?

#### Create a Virtual env in the local and activate it
```bash
conda create -n visa python=3.8 -y
```

```bash
conda activate visa
```

#### Install required libraries
```bash
pip install -r requirements.txt
```

#### Run the app
```bash
python app.py
```


## Workflow

1. Constant ==> To store all the model related files names and directories
2. Config_Entity ==> Have the required input files-names/directories to each entity
3. Artifact_Entity ==> Have the required output files-names/directories of each entity 
4. Component ==> each task is divided into a component 
5. Pipeline ==> Complete ML Lifecycle
6. App.py / Demo.py 


## Initial Setup

### Create MongoDB Account
* MongoDB: https://account.mongodb.com/account/login

### Export the  environment variable
```bash
export MONGODB_URL="mongodb+srv://<username>:<password>...."

export AWS_ACCESS_KEY_ID=<AWS_ACCESS_KEY_ID>

export AWS_SECRET_ACCESS_KEY=<AWS_SECRET_ACCESS_KEY>
```



# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in AWS


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo to store/save docker image
    - Save the URI: XXXXXXXXXXXXX.dkr.ecr.us-east-1.amazonaws.com/mlproject (Example)

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting ==> actions ==> runner ==> new self hosted runner ==> choose os ==> then run command one by one


# 7. Setup github secrets:

   - AWS_ACCESS_KEY_ID
   - AWS_SECRET_ACCESS_KEY
   - AWS_DEFAULT_REGION
   - ECR_REPO

    
