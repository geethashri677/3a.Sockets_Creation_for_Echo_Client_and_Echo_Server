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
client:
import socket

s = socket.socket()

s.connect(('localhost', 8080))

while True:
    msg = input("Client > ")

    s.send(msg.encode())

    if msg == "exit":
        break

    print("Server >", s.recv(1024).decode())

s.close()
server:
import socket

s = socket.socket()

s.bind(('localhost', 8080))

s.listen(1)

print("Server waiting for connection...")

c, addr = s.accept()

print("Connected with:", addr)

while True:
    client_message = c.recv(1024).decode()

    if client_message == "exit":
        print("Connection closed")
        break

    print("Client >", client_message)

    reply = input("Server > ")

    c.send(reply.encode())

c.close()
s.close()
## OUTPUT
<img width="1912" height="1020" alt="Screenshot 2026-05-21 140014" src="https://github.com/user-attachments/assets/5c4f65b3-eeb2-406b-8521-b9aecdb546c9" />
<img width="1918" height="1022" alt="Screenshot 2026-05-21 140022" src="https://github.com/user-attachments/assets/935b9fef-0f45-49c9-b16c-ce04373ae0b5" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
.
















.




















.












.






.
