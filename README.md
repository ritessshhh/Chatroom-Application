# Writing an explanation of the chatroom application in Markdown format

# Chatroom Application in C++

This document explains the functioning of a simple chatroom application implemented in C++ using socket programming. The application consists of two parts: a server and a client.

## Server Code

The server side of the application performs the following tasks:

1. **Socket Creation:** It starts by creating a socket using the `socket` function.
2. **Setting Socket Options:** The `setsockopt` function is used to attach the socket to the server port (8080 in this case).
3. **Binding:** The `bind` function binds the server to a specific address and port.
4. **Listening:** It listens for incoming connections using the `listen` function.
5. **Accepting Connections:** The server accepts a connection using the `accept` function.
6. **Communication Loop:**
   - The server reads messages sent by the client using the `read` function.
   - It then echoes back the received message to the client using the `send` function.
   - If the received message is "exit", the server breaks the loop and closes the connection.

## Client Code

The client side of the application performs these operations:

1. **Socket Creation:** It creates a socket similar to the server.
2. **Connecting to the Server:** The client uses the `connect` function to connect to the server at the specified IP address and port.
3. **Communication Loop:**
   - The client sends messages to the server using the `send` function.
   - It then waits to receive a message from the server, which is an echo of the sent message.
   - If the user types "exit", the client breaks the loop and the connection is closed.

## Conclusion

This basic chatroom application demonstrates the fundamentals of network programming in C++, particularly socket programming. The server and client communicate over TCP, with the server echoing back whatever message the client sends.

