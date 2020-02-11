#1 -  Build it
docker build -t mongodb . 


# 2 - After that, we can get a list of the images on our docker host 
#     with the docker images sub-command
#     We can see the MongoDB image, we've just created in the list
docker images

# 3 - We can use the docker rmi subcommand, which stands for remove image.
#     we get an error because there are container around are based on this image.
#     because the container won't be able to start if we remove the image.
docker rmi temp



# 4 - So I'm going to add the -d flag, which stands for detach.
#   - That way after the container launches we'll be dropped back to the shell,
docker run -d -p 27017:27017 -p 28017:28017 --name mongo mongodb


#5 - Current Running Docker  - PS is standing for process status
docker ps


#6 - View Docker Log, xxx is the starting words of id, or docker name  
docker logs  xxx



#7 - Connect Docker by mongo
mongo 



#8 - Running Mongo in the docker
docker exec -it mongo /bin/bash 


#9 - View current process
ps aux

#10 - Exit
exit


#11 - Stop the Docker
docker stop mongo


#12 - Run mongo again
docker start mongo

#13 - remove docker by spfic id
docker rm mongo

#14 - Mongo Container will be gone from the list
docker ps -a




