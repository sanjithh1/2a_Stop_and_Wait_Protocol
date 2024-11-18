# EXP : 2a_Stop_and_Wait_Protocol


## NAME : MOHAMED HAMEEM SAJITH J
## REG NO : 212223240090


## AIM :
To write a python program to perform stop and wait protocol

## ALGORITHM :

1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
7. 
## PROGRAM :

### CLIENT :

```
NAME: Mohamed Hameem Sajith J
REG NO: 212223240090

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
### SERVER :

```
NAME: Mohamed Hameem Sajith J
REG NO: 212223240090

import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    print(s.recv(1024).decode())
    s.send("Acknowledgement Recived".encode())

```
## OUTPUT :

### CLIENT :
![image](https://github.com/user-attachments/assets/d0e9c470-bd9b-4f59-afee-877f858d77e8)

### SERVER :
![image](https://github.com/user-attachments/assets/90b4da62-e015-468a-9d47-b267d2369ab8)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
