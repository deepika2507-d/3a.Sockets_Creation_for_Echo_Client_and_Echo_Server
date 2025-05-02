# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM

# client.py
import socket

s = socket.socket()
s.connect(('localhost', 8000))

while True:
    msg = input("Client > ")
    s.send(msg.encode())
    print("Server > ", s.recv(1024).decode())
# server.py
import socket

s = socket.socket()
s.bind(('localhost', 8000))
s.listen(5)

c, addr = s.accept()

while True:
    ClientMessage = c.recv(1024).decode()
    c.send(ClientMessage.encode())


## OUTPUT
cilent

![image](https://github.com/user-attachments/assets/5d8539f7-9346-40bc-af1e-640cb28350aa)

server

![image](https://github.com/user-attachments/assets/dbc018a0-1020-4cb8-a9cb-2d828c984e67)



## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
