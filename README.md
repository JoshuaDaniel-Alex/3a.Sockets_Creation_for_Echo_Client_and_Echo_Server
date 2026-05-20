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
## PROGRAM:
Client:
```
# Developed by:Joshua Daniel A
# Register number:212225040161
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
Server:
```
# Developed by:Joshua Daniel A
# Register number:212225040161
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    ClientMessage=c.recv(1024).decode() 
    c.send(ClientMessage.encode())
```
## OUPUT:
Client:
<img width="1126" height="396" alt="Screenshot 2026-05-20 084002" src="https://github.com/user-attachments/assets/73b09daa-ec44-47f0-bff2-15686f0476f9" />

Server:
<img width="1102" height="289" alt="Screenshot 2026-05-20 084017" src="https://github.com/user-attachments/assets/75c83d2a-d09f-4851-9148-eaff35501056" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
