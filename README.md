# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
<br>

# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
<br>

## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
   
<br>

## PROGRAM
## Client 
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## Server
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
<br>

## OUPUT
## Client

![image](https://github.com/user-attachments/assets/c64b4f21-b0e8-4c13-8b51-4aa2e4c7283c)
<br><br><br><br><br>
## Server

![image](https://github.com/user-attachments/assets/e55f3341-b86f-4d1a-860c-e382f4ad3515)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
