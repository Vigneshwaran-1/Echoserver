# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
server
~~~
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_server((HOST, PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'Connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)
~~~~
client
~~~~
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'Vignesh,212224040358')
    print(f'Received: {s.recv(1024)!r}')
~~~

## OUTPUT:
server
~~~~
<img width="359" alt="server sshot" src="https://github.com/user-attachments/assets/9e946a69-861c-4d1d-b378-0232de7511c9" />
~~~
client
~~~~
<img width="344" alt="client sshot" src="https://github.com/user-attachments/assets/096c9509-899c-465d-bdc7-4fe2ccc7049e" />
~~~~



## RESULT:
The program is executed successfully
