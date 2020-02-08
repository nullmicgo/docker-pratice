FROM ubuntu
ENV appDir=/app message="Welcome to our app!"
WORKDIR $appDir
RUN echo $message > README.txt
CMD echo Read ${appDir}/README.txt for a friendly greeting!