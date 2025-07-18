# Medical_chatbot_generativeAI


# How to run?
### STEPS:

Clone the repository

```bash
Project repo: https://github.com/DeeptiShuklaProject/Medical_chatbot_generativeAI.git
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n medibot python=3.10 -y
```

```bash
conda activate medibot
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```
### Create a `.env` file in the root directory and add your Pinecone & openai credentials as follows:




```bash
# run the following command to store embeddings to pinecone
python store_index.py
```

```bash
# Finally run the following command
python app.py
```

Now,
```bash
open up localhost:
```


### Techstack Used:

- Python
- LangChain
- Flask
- GPT
- Pinecone


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
   - PINECONE_API_KEY
   - OPENAI_API_KEY

    

# 8. Troubleshoot
(medibot) D:\Medical_chatbot_generativeAI>python
Python 3.10.18 | packaged by Anaconda, Inc. | (main, Jun  5 2025, 13:08:55) [MSC v.1929 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> from pathlib import Path
>>> p = "test/t.py"
>>> Path(p)
WindowsPath('test/t.py')
>>> import os
>>> os.path.split(p)
('test', 't.py')
>>>



then go to setup.py and write below code
from setuptools import find_packages, setup

setup(
    name = 'Medical_chatbot_generativeAI',
    version= '0.0.0',
    author= 'DeeptiShuklaProject',
    author_email= 'deeptishukla515@gmail.com',
    packages= find_packages(),
    install_requires = []

)

# add reuirements.txt .....    -e . then run pip install.r requirements.txt 
then check pip list 
showing project name like "Medical_chatbot_generativeAI 0.0.0       d:\medical_chatbot_generativeai"