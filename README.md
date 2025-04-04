# Python Socket Tutorial 

![icon](https://www.tutorialspoint.com/python/images/connection.jpg)

Python Socket Programming

Socket programming is a technique in which we communicate between two nodes connected in a network where the server node listens to the incoming requests from the client nodes.

In Python, the socket module is used for socket programming. The socket module in the standard library included functionality required for communication between server and client at hardware level.

This module provides access to the BSD socket interface. It is available on all operating systems such as Linux, Windows, MacOS.
# What are Sockets?

Sockets are the endpoints of a bidirectional communications channel. Sockets may communicate within a process, between processes on the same machine, or between processes on different continents.

A socket is identified by the combination of IP address and the port number. It should be properly configured at both ends to begin communication.
connection IP_address

Sockets may be implemented over a number of different channel types: Unix domain sockets, TCP, UDP, and so on. The socket library provides specific classes for handling the common transports as well as a generic interface for handling the rest.

The term socket programming implies programmatically setting up sockets to be able to send and receive data.



# There are two types of communication protocols −

    connection-oriented protocol

    connection-less protocol

TCP or Transmission Control Protocol is a connection-oriented protocol. The data is transmitted in packets by the server, and assembled in the same order of transmission by the receiver. Since the sockets at either end of the communication need to be set before starting, this method is more reliable.

UDP or User Datagram Protocol is connectionless. The method is not reliable because the sockets does not require establishing any connection and termination process for transferring the data.
Python socket Module

The socket module is used for creating and managing socket programming for the connected nodes in a network. The socket module provides a socket class. You need to create a socket using the socket.socket() constructor.

An object of the socket class represents the pair of host name and the port numbers.
Syntax

The following is the syntax of socket.socket() constructor –

socket.socket (socket_family, socket_type, protocol=0)


Parameters

    family − AF_INET by default. Other values - AF_INET6 (eight groups of four hexadecimal digits), AF_UNIX, AF_CAN (Controller Area Network) or AF_RDS (Reliable Datagram Sockets).

    socket_type − should be SOCK_STREAM (the default), SOCK_DGRAM, SOCK_RAW or perhaps one of the other SOCK_ constants.

    protocol − number is usually zero and may be omitted.

Return Type

This method returns a socket object.

Once you have the socket object, then you can use the required methods to create your client or server program.
Server Socket Methods

The socket instantiated on server is called server socket. Following methods are available to the socket object on the server −

    bind() method − This method binds the socket to specified IP address and port number.

    listen() method − This method starts server and runs into a listen loop looking for connection request from client.

    accept() method − When connection request is intercepted by server, this method accepts it and identifies the client socket with its address.
