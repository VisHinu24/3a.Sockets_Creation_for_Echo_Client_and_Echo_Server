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

Client :
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    clientmessage=c.recv(1024).decode()
    c.send(clientmessage.encode())
```

Server:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client>")
    s.send(msg.encode())
    print("server>",s.recv(1024).decode())
```

## OUPUT

Client :
![Screenshot 2024-04-22 201149](https://github.com/VisHinu24/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/144244396/93a376ec-91a0-4605-abb7-c42919374686)

Server:
![Screenshot 2024-04-22 201144](https://github.com/VisHinu24/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/144244396/133556aa-511e-414e-ab9b-4ad6ea9edbd3)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
