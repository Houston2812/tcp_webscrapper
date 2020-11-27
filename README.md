# TCP based webscrapping service
The service has the following structure: 
* Server
    * Scrapper
* Client

## Server
The connection between the client and server is established using TCP.  
Server has a threaded struture, so that it is able to serve multiple clients and the same moment.   
The server receives url of some arbitrary website and scraps it to determine the numbe of the images and leaf paragraphs.
When the required result is obtained respince is sent back to the client.  

To run the server following command is used:  
&nbsp;&nbsp;&nbsp; _python webscrapper.py server_
  
Following options are available:  
* --host "host"  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Provides an interface for server to listen to. Default value is 127.0.0.1.
* --port port  
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Provides port for server to listen. Default value is default TCP port - 1060  (should be integer).

## Client
Client is able to send reqests containg any arbitrary url to the server, in order to get the results of webscrapping.
To run the script as a client the following command in used:  
&nbsp;&nbsp;&nbsp; _python webscrapper.py server -p url_

Following runnning option are available:
* --host "host"

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Provides an host to the client to connect to. Default value is 127.0.0.1.
* --port port

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Provides a port to the client to connect to. Default value is default TCP port - 1060 (should be integer).
* -p url

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Page option is used to provide and url to the server. This option is mandatory, so that server will be able to handle request. 