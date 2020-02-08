
#1  - We can confirm all this by building our container with this
docker build -t temp .


#2 - Running it with docker run temp
docker run temp cat /app/README.txt


#3 - Use -it to set up an indirect of terminal session
#    Run the temp image      
docker run -it temp /bin/sh
