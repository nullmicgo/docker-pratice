docker pull ubuntu

# -i <--- interactive session on the container
docker run -it --detach --name=container1 ubuntu

docker run -it --detach --name=container2 ubuntu


172.17.0.2


#open a shell session
docker attach container1
ping 172.17.0.3 <---fail

#need to install the ping command using apt-get
apt-get update

#install ping command
apt-get install iputils-ping

#Ping Again
ping 172.17.0.3 <---success