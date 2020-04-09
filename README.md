# Simple-Socket
_Made for CS3700, Networks and Distributed Systems._

##NOTE##: I cannot publicly post this unless requested specifically.

This is a simple socket program that communicates with a server that delegates string counting or sorting tasks.
Socket is run on a TCP (Transmission Control Protocol) bound port (27993 default) and accepts these commands:
- FIND: Counts the number of occurrences of a particular string in a message.
- BYE: Records and prints out the given secret flag and closes the connection.

The server will accept these commands:
- HELLO: Opens connection to the socket.
- COUNT: Determines if the given number of string occurrences is correct and continues.

After the HELLO, the server will send multiple FIND requests to the socket and if they are all answered correctly, returns the secret flag.

Command line syntax:
$ ./client <-p port> <-s> [hostname] [NEU ID]
