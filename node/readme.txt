###########################
Change into the directory that has your Dockerfile. 
Then use the docker build command, with the -t option set to node-js-app to tag the image. We'll tell it that the Dockerfile is in the current directory: .
###########################
docker build -t node-js-app .



###########################
We have the image; let's try running it as a container! 
We'll use the docker run command. 
The container will have port 80 exposed, 
so we need to publish it as a port on our Docker host. 
I'll pass the -p option to publish it, 
and map the host port of 8080 to the exposed container port 80.
 I'll pass the -d flag to detach the container from the terminal, 
 so we can run other commands. And of course, 
 I need to specify which image to run: node-js-app.
###########################
docker run -p 8080:80 -d node-js-app



###########################
If we run docker ps, we'll see a container based on the node-js-app image in the output.
###########################
docker ps




###########################
If we take the container ID shown there, and pass it to docker logs, we can see our app's output.
###########################
docker logs ID_HERE




###########################
We can execute additional processes on the container with docker exec. 
If we want to open a shell on the container, we can use -it to set up an interactive terminal session, specify the container ID as the container to run on, and specify /bin/bash as the executable to run.


###########################
docker exec -it ID_HERE /bin/bash

