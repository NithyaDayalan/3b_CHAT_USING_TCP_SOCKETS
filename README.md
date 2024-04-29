# 3b  CREATION FOR CHAT USING TCP SOCKETS
## DEVELOPED BY : NITHYA D
## REG.NO : 212223240110

## AIM :
To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM :
1. Import the necessary modules in python.
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in server.
4. Send and receive the message using the send function in socket.

## PROGRAM :
### CLIENT :
```
Developed by : NITHYA D
Reg.no : 212223240110

import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
   msg=input("Client > ") 
   s.send(msg.encode()) 
   print("Server > ",s.recv(1024).decode())
```
### SERVER :
``` 
Developed by : NITHYA D
Reg.no : 212223240110

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

## OUTPUT :
![image](https://github.com/NithyaDayalan/3b_CHAT_USING_TCP_SOCKETS/assets/166380061/6842d83c-e228-4981-9a7b-b0a9c276bd7d)

## RESULT :
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
