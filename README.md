# Socket-programming

This is a simple client-server model where a client program can chat with a dummy math server. The communication between client and server goes as follows:

*	The server gets started first and listens to a known port.
*	The client program is started as server IP and port is provided in the command line.
*	The client connects to the server and asks for user input. The user enters simple arithmetic expression as “7+5”,"5*3","10/2" or “10-2”. The input is sent to the server through connected socket.
*	The server receives the input from the client socket, evaluate the expression and sends the result back to the client.
*	The client should display the result from the server to the user and prompts for the next input, until the user terminates the client program by Ctrl+C.


### Singleclient:
Server program [Server.c](https://github.com/thrylos2307/Socket-programming/blob/master/singleclient/server.c) is a single process server that can handle only one client at a time. An  client program is in [client.c](https://github.com/thrylos2307/Socket-programming/blob/master/singleclient/client.c)

### Multiclient:
Server program [Server.c](https://github.com/thrylos2307/Socket-programming/blob/master/multiclient/server.c) is a multi-process server that forks a process whenever it receives a new client request. Multiple server will be able to chat with the server concurrently.  An  client program is in [client.c](https://github.com/thrylos2307/Socket-programming/blob/master/multiclient/client.c)


#### Running Program:
First start the server then client can be connected....
* Server: 
-> gcc server.c -o server <br>
->./server [port no.]

* Client:
-> gcc client.c -o client<br>
-> ./client 127.0.0.0 [port no.]

Note: port number for client and should be same.
