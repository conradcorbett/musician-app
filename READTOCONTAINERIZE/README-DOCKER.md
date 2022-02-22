Follow these steps to dockerize the nodejs app, then push your image to your docker hub account

Clone the github repo to your local CentOS7 machine
    
    # sudo git clone https://github.com/conradcorbett/musician-app.git

Install docker and start the service
    
    # sudo yum install docker
    # sudo sysetmctl start docker
    # sudo sysetmctl status docker

Create Dockerfile in directory, see Dockerfile

Build docker image
    
    # docker build -t nodejs-test-app:latest .
    # docker images

Run docker image

    # docker run -it -d -p 80:3001 nodejs-test-app:latest
    # docker ps

Create empty docker repo by logging into docker.com web GUI, then push your image to the repo you created on docker hub

    # docker login
    # docker tag nodejs-test-app:latest conradcorbett/nodejstest:latest
    # docker push conradcorbett/nodejstest:latest

To run the container on another server, make sure docker is installed:

    # docker pull conradcorbett/nodejstest:latest
    # docker tag docker.io/conradcorbett/nodejstest:latest mynodeapp:latest
    # docker run -it -d -p 80 mynodeapp:latest