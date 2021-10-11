# Sockets

```python
import sys,socket,time

ip = "127.0.0.1"
ports = [80,443]

for port in ports:
        s = socket.socket(socket.AF_INET,socket.SOCK_STREAM)
	s.connect((ip , port))
        sleep(2)
        s.send("GET / HTTP 1.1")
        print("HTTP GET Request :")
	s.recv(1024)
        s.close()
```
