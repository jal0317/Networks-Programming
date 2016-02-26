
CSCE 3530 - Introduction to Computer Networks

Spring 2016 - Instructor: Garima Bajwa

-----------------------------------------------------------------------------------


Authors:

Skylar Griffis

Jordan Luper

-----------------------------------------------------------------------------------


Program Purpose:

This program has two main parts. These parts are a 
web server and a single-threaded web proxy. The web server (server.c)
and the web proxy (proxy.c) are each run on seperate cse machines at the
same time. Through a web browser, users can make an HTTP request with a 
special URL to the web proxy for a website. The proxy will then make the
same HTTP request to the server. The server will process the HTTP request
it recieves from the proxy, fetching the web page object. The server will
send this object as an HTTP response to the proxy, and the proxy will
send the same HTTP response back to the web browser so that the user can
view the web page.


-----------------------------------------------------------------------------------

Program Contents:

server.c

proxy.c



-----------------------------------------------------------------------------------

Running:

Remotely access two different CSE machines in seperate windows
In one window (cse01.cse.unt.edu), run server.c:

	g++ server.c
	./a.out
	
In the other window (cse02.cse.unt.edu), run proxy.c 
AFTER running the server successfully:

	g++ proxy.c
	./a.out
	
Open a web browser, and type the following URL into your browser,
replacing "www.website.net" with a website of your choosing.

	cse02.cse.unt.edu:9999/www.website.net
	
make sure that the cse machine you enter in this URL is the one
that you are running your proxy server on.
