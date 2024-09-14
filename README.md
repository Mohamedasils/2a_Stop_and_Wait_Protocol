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

NAME : MOHAMED ASIL S
REGISTER NO : 212223040112

## CLIENT:

```

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

## SERVER:

```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    print(s.recv(1024).decode())
    s.send("Acknowledgement Recieved".encode())

```
## OUTPUT

![image](https://github.com/user-attachments/assets/bfcaefd1-8f03-451d-9092-ea29b43a5f32)



![image](https://github.com/user-attachments/assets/e61ea377-85c3-4556-a37b-37bac81d23cf)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
