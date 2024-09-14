# 2a_Stop_and_Wait_Protocol
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
## Client
```
Name:Sanjith.R
Reg no:212223230191

import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    i=input("Enter a data: ")
    c.send(i.encode())
    ack=c.recv(1024).decode()
    if ack:
        print(ack)
        continue
    else:
        c.close()
        break
```
## Server
```
Name :Sanjith.R
Reg no:212223230191

import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    print(s.recv(1024).decode())
    s.send("Acknowledgement Recived".encode())
```
## OUTPUT
## client
![image](https://github.com/user-attachments/assets/632cc16c-8287-4cb1-9a9e-f1396863f31c)

## Server

![image](https://github.com/user-attachments/assets/3d41e9e0-a2b2-4a97-bb4f-54677fdf6b37)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
