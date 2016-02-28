
CSCE 3530 - Introduction to Computer Networks

Spring 2016 - Instructor: Garima Bajwa

-----------------------------------------------------------------------------------


Authors:

Skylar Griffis

Jordan Luper

-----------------------------------------------------------------------------------


Program Purpose:

This program has two main parts. These parts are a 
web server and a multi-threaded web proxy. The web server (server.c)
and the web proxy (proxy.c) are each run on seperate cse machines at the
same time. Through a web browser, users can make an HTTP request with a 
special URL to the web proxy for a website. The proxy will then make the
same HTTP request to the server. The server will process the HTTP request
it recieves from the proxy, fetching the web page object. The server will
send this object as an HTTP response to the proxy, and the proxy will
send the same HTTP response back to the web browser so that the user can
view the web page.

Unfortunately, we were unable to implement this in two parts. Instead, we
made a proxy webserver that functions as one program and acheives the same
results. The proxy webserver recieves an HTTP request through the browser via
a specific URL (see "Running:" below). The proxy webserver fetches the HTML page
from the host specified (see "Running:" below, 'www.website.net'). The proxy
webserver then serves the HTML page to the web browser which requested it. The
proxy is multi-threaded to handle multiple requests.

-----------------------------------------------------------------------------------

Program Contents:

server.c
readme.txt


-----------------------------------------------------------------------------------

Running:

Remotely access two different CSE machines in seperate windows
In one window (cse01.cse.unt.edu), run server.c:

	gcc server.c
	./a.out PORTNUMBER
	
Open a web browser, and type the following URL into your browser,
replacing "www.website.net" with a website of your choosing and
PORTNUMBER with the same port number you entered to run the server.

	cse02.cse.unt.edu:PORTNUMBER/www.website.net
	
make sure that the cse machine you enter in this URL is the one
that you are running your server on.
