# docker-node-demo-app
A docker file to run a demo nodejs app

The docker file is already written in the app directory

Navigate to the app directory

`cd app`

### build the image and give it a name

`docker build . -t appimage`

Check your images to confirm the appimage created

`docker images`

### Run a container from the image and give it a name

`docker run -dt --name app01 appimage`

Check for the running container

`docker container ls`

Check the ip address of the container 

`docker inspect app01 | grep IPAddress`

### Check if the app is running 

The app runs on port 8080

`curl http://<ipaddress>:8080`

Open your browser to open the app on

`http://<ipaddress>:8080`
