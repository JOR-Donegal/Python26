# TCP

When we need reliable data communications, we use Transmit Control Protocol (TCP). The client and server in this communication have a complex network stack. Every communication is acknowledged, and functionality exists within the protocol for it to auto-tune to the characteristics of the communication medium.&#x20;

First, I create **tcp\settings\tcp.py**

```python
TCP = {
    "SERVER_TCP_IPv4": '127.0.0.1',
    "SERVER_PORT": 23
}
```

Then I create **tcp\client.py**

```
'''
TCPClient by: JOR
Send TCP packets to a particular address and port.
Alpha: 13FEB22
'''

import socket
import time
from datetime import datetime
import settings.tcp as settings

TCP_IP = settings.TCP["SERVER_TCP_IPv4"]
TCP_PORT = settings.TCP["SERVER_PORT"]

print(f'This is the TCP client, it will try to connect to a server at {TCP_IP}:{TCP_PORT} in the settings file.')
print('This script has no error handling, by design')

BUFFER_SIZE = 1024
while True:
    print(f'Trying to open a socket to {TCP_IP}:{TCP_PORT}')
    with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
        message_text = f"ATU {datetime.now()}"
        message = message_text.encode('utf-8')
        s.connect((TCP_IP, TCP_PORT))
        s.send(message)
        print(f'Sent {message_text} to {TCP_IP}:{TCP_PORT}')
        data = s.recv(BUFFER_SIZE)
        print('Server echoed:', data)
        time.sleep(1)

```

Then I create **tcp\_server.py**

```python
'''
TCPServer by: JOR
Listens for packets on a particular address and port.
Alpha: 13FEB22
'''

import socket
import settings.tcp as settings

TCP_IP = settings.TCP["SERVER_TCP_IPv4"]
TCP_PORT = settings.TCP["SERVER_PORT"]
BUFFER_SIZE = 1024

print(f'This is the TCP server, it will open a port at {TCP_IP}:{TCP_PORT} and being listening')
print(f'Make sure the actual server IP address matches {TCP_IP} in the settings file')
print('This script has no error handling, by design')

try:
    with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
        s.bind((TCP_IP, TCP_PORT))
        print(f'Bound to {TCP_IP}:{TCP_PORT}')
        while True:
            s.listen(1)
            conn, addr = s.accept()
            print(f'Connection address: {addr}')
            data = conn.recv(BUFFER_SIZE).decode()
            print(data)
            conn.send(data.encode())
except socket.error as e:
    print(f'Error: {e}')
```

## Testing

To make this work, I run the programs in two separate console sessions. I must press **\[ctrl]\[c]** to exit. I start the server first; it will listen indefinitely.

<figure>
<img src = "https://jor-donegal.github.io/Python26/images/fig49.jpg">
<figcaption>Fig 49. Server output.</figcaption>
</figure>


I start the client next. I need to do it in this order. The client tries to make a connection to a definite end point. There is no error handling, so if the connection is not available, it times out and exits.

<figure>
<img src = "https://jor-donegal.github.io/Python26/images/fig50.jpg">
<figcaption>Fig 50. Client output.</figcaption>
</figure>


If you cannot exit using \[ctrl]\[c], just close the command window.

Whenever you see **b’something’** this indicates that Python is handling bytes. This is normal in communications, but you may have to do some conversions to and from strings.
