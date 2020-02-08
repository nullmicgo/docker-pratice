FROM ubuntu

RUN useradd michael

WORKDIR /app

# Using root user to 
# change the owner of the app directory to michael user
RUN chown michael /app

# Using Spefiic User for the docker command
# USER won't create the user for us
USER michael



# Before running this,
# make sure this user got the permission
# to create the folder
RUN whoami > whoami.txt


CMD whoami