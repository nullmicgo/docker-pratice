It's a really simple app consisting of a single file.
All it does is listen for browser requests on port 8080 and respond with hello from Python.
But even something this simple introduces a dependency,

we have to have Python 3 installed in order to run it.
And it looks like this machine only has Python 2 installed.

So we get an error when we try to launch this app.py program, python app.py.
#Error start from here
        Traceback (most recent call last):
        File "app.py", line 3, in <module>
            from http.server import BaseHTTPRequestHandler, HTTPServer
        ImportError: No module named http.server
#Error end from here


command:
#1
docker build -t sample-web-app .

#2 - Check is the image exist
docker images

#3 - run it in 8080 port by sample-web-app image
docker run -p 8080:8080 sample-web-app

#4 - 
Open Browser with 'http://localhost:8080/' URL, 
then you will see the following message
Hello from Python!
