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
 c.send(ClientMessage.encode())
```

## OUPUT
## CLIENT 
![325084640-23aa34f5-d9be-485c-a69a-6f188a415e03](https://github.com/lekasri12/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/149037427/abbd27b8-061a-49e7-ba10-85f73f22f4e9)

## SERVER
![325084705-7c342bbf-7e4d-4838-8e8a-973f0743037a](https://github.com/lekasri12/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/149037427/f1fd1cfb-32b8-4278-8366-65b50ed5544a)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
