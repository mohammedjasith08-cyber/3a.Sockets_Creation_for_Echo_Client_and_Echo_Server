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
```
Name:MOHAMMED JASITH J
Reg no:212225230180
```
Client
```
import socket

s = socket.socket()
s.bind(('localhost', 6000))
s.listen(5)

c, addr = s.accept()

while True:
    ClientMessage = c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
Server 
```
import socket

s = socket.socket()
s.connect(('localhost', 6000))

while True:
    msg = input("Client > ")
    s.send(msg.encode())
    print("Server > ", s.recv(1024).decode())  
```
## OUPUT
<img width="1920" height="1080" alt="Screenshot (37)" src="https://github.com/user-attachments/assets/4625e2cf-05de-4c82-b6d0-8f4a7043dcc8" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
