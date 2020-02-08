
#1  - We can confirm all this by building our container with this
docker build -t temp .


#2 - Running it with docker run temp
docker run temp cat /app/README.txt


#3 - Use -it to set up an indirect of terminal session
#    Run the temp image      
docker run -it temp /bin/sh

#4 - If we run the set command, we'll see the settings for
#    all our environment variables.
set

#5 - Testing Echo Environemnt variables
echo $appDir


#5 - Testing Echo Environemnt Message
echo ${message}

