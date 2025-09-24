# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.

```
NAME:GURUPARAN G
REG NO:212224220030
```
## PROGRAM

### client.py
```python
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
### server.py
```python
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


## OUPUT

<img width="1917" height="1133" alt="Screenshot 2025-09-22 115231" src="https://github.com/user-attachments/assets/2a377fce-9bcc-47c2-98cb-0a3d17b6fbdc" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
