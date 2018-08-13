# py-server-examples
Simple python web server examples for demonstration and teaching. 

### Usage


```
 cd server-wsgi
 python server.py
```

This will serve at [http://localhost:8000/](http://localhost:8000/).

To stop serving, simply type `Ctrl+c` in the terminal. The web server will keep running if you don't explicitly kill it.

To run other implementations, kill the version you have open, `cd` into another directory, and run `python server.py`. 

Note that these examples are all written for python3.   

## Server Implementations  
The goal of this repo is to demonstrate various ways to set up a web server using Python, and to use some of the lower-level approaches to demonstrate what the server is doing. 

#### server-simple 
The simple-server is quite rudimentary. An HTML form is rendered, and a server will log the user's input. This example represents a static internet. 
Using this repo together with server-cgi, one can learn about GET and POST, and begin to understand what the client and server each do.
The server-simple implementation makes use of `http.server.SimpleHTTPRequestHandler`. 
   
#### server-cgi 
The simple-cgi is quite basic, making use of Common Gateway Interface (CGI). This was standard in the 1990's. Using CGI allows scripts to be run server-side. 
In this example, the input from an HTML form is parsed by a server-side python script, which returns an HTML response, which is then rendered in the browser. 
The server-simple implementation makes use of `http.server.CGIHTTPRequestHandler`. 
CGI is an outdated methodology for web servers, which today is problematic in many ways. It is included here solely for demonstrative purposes, and should not be used.   

#### server-wsgi
The server-wsgi implementation gets us towards the state of the art, making use of Web Server Gateway Interface (WSGI).
WSGI is a specification for an application and server to communicate with one another. The code is therefore more abstract than in the previous examples. 
This example uses the reference implementation of the WSGI specification which ships with Python, called `wsgiref`.
While one would generally _not_ use a "raw" implementation as is done here, modern python frameworks are built using this standard.

#### server-flask 

To run flask, first you will have to [install flask](http://flask.pocoo.org/docs/1.0/installation/#installation). 
Using Anaconda and PyCharm, the easiest way forward is to: 
* Choose a Python environment in Anaconda and install Flask
* In PyCharm, open Preferences/Settings --> Project --> Project Interpreter, and makes sure that the version of python which is installed 
in the environment which you chose in Anaconda is chosen.
* In PyCharm, run server-flask/server.py.  

 

