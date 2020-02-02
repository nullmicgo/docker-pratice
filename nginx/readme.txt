# 1 - We'll retrieve the NGINX image from the Docker registry with, docker pull nginx.
docker pull nginx

# 2 - Then we can use the docker inspect command on the nginx image to confirm
      which port it exposes, with docker inspect nginx.
docker inspect nginx

# 3 - Create a container frmo the image using the docker run command
      --detach <-- adding this option will leave the container running in the background 
docker run -p 8080:80 --detach nginx

#4 - Check the process Status (ps)
docker ps

#5 - go visit localhost:8080 and see the niginx default page

#6 - check docker network
docker network ls


#7 - See Various info about the network
docker network insepect bridge

#8 - Stop Docker process by id
docker stop 4d85383fc4d2

#9 - We can see the bridge is not inthe bridge network
docker network insepect bridge