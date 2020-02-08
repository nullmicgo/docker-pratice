docker build -t temp .

docker run temp



# check the app directory at the top
docker run temp ls -l /


# check the whoami.txt is also owned by michael user
docker run temp ls -l /app

# Show us that the current user was michael when the text file was written
docker run temp cat whoami.txt