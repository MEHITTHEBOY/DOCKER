# DOCKER
STEP1: INSTALL DOCKER
sudo apt update 
sudo apt install docker.io -y

STEP2: CHECK IF DOCKER IS WORKING
docker --version

STEP3: INCASE OF ANY ISSUE , CREATE A DOCKER GROUP AS SHOWN BELOW
sudo usermod -aG docker $USER

newgrp docker

STEP4: SETUP YOUR PROJECT
Suppose there is a folder you created named practice, so in this step assumed you're in practice folder
Create index.js

Create Dockerfile
--->
    FROM node:alpine
    
    COPY . /practice
    
    CMD ["node", "/practice/index.js"]

STEP5: BUILD THE DOCKER IMAGE
docker build -t practice .

STEP6: RUN THE DOCKER CONTAINER
docker run practice

STEP7: CHECK DOCKER IMAGES OR DOCKER CONTAINERS
docker images 

docker ps -a
