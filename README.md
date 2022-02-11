# musician-app

To run nodejs web application in CentOS7:
1) Install nodejs in Centos7 VM:
    # curl -sL https://rpm.nodesource.com/setup_10.x | sudo bash -
    # sudo yum install nodejs
2) Clone App from github repo:
    # sudo git clone https://github.com/conradcorbett/musician-app.git
3) This app needs Express, which helps manage packages for nodejs. Installing express adds the necessary modules
    # npm install express --save
4) Open firewall port in Centos7
    # firewall-cmd --permanent --zone=public --add-port=3001/tcp
    # firewall-cmd --reload
5) Run the app, there are two ways to do this:
A) # node app.js
    This will run the app.js file directly
B) # npm start
    This will call the start script located in package.json, preferred method to start app
6) If you need to kill the process:
    sudo netstat -nlp | grep :3001
    kill <pid>


NodeJS / React sample app for AWS CI/CD pipeline tutorial

https://www.youtube.com/watch?v=NwzJCSPSPZs
