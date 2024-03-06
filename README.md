# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## CLIENT
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## SERVER
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```
## OUTPUT

## CLIENT
![243810764-aaac8d82-765c-434a-b873-833a20d6fade](https://github.com/Jai-1801/3b_CHAT_USING_TCP_SOCKETS/assets/139335300/85abe304-a514-4f31-b5ff-63bd56cc63d9)

## SERVER
![243810819-05c7629a-2407-441e-b734-4d63a46d37d7](https://github.com/Jai-1801/3b_CHAT_USING_TCP_SOCKETS/assets/139335300/7b2dba33-6a1f-48c4-9886-a70198f8d21b)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

