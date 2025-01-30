# LLM-Apps-with-Chainlit



Create a repository in GitHub

# How to Run in own local Machine?

### STEPS:
- Clone the repository in selected specific drive in own Local Machine.
- open the Terminal 

```
Project repo: https://github.com/
```

```cmd
git clone <copied link from github>
``` 

- To open in selected folder. 
```cmd
cd <Hit folder name>
```

### STEP 01- Create a conda environment after opening the repository

```cmd
conda create -n chainlitDemo python=3.8 -y
```

```cmd
conda activate chainlitDemo
```

### STEP 02- Install the Requirements
```cmd
pip install -r requirements.txt
```


```cmd
git add .
```

```cmd
git commit -m "folder structure added"
```

```cmd
git push origin main
```


### Create a `.env` file in the root directory and add your Pinecone & openai credentials as follows:

```
OPENAI_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
```



```cmd
# Finally run the following command
python app.py
```

Now,
```cmd
open up localhost:
```


### Techstack Used:

- Python
- Chainlit
- OpenAI


# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


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
    - Save the URI: 970547337635.dkr.ecr.ap-south-1.amazonaws.com/medicalchatbot

	
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
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

   - AWS_ACCESS_KEY_ID
   - AWS_SECRET_ACCESS_KEY
   - AWS_DEFAULT_REGION
   - ECR_REPO
   - OPENAI_API_KEY

    
