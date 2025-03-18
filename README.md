# EX01 Developing a Simple Webserver
## 212224040319
## Date:11.03.2025

## AIM:
To develop a simple webserver to serve html pages and display the list of protocols in TCP/IP Protocol Suite.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Import the necessary modules.

### Step 5:
Define a custom request handler.

### Step 6:
Start an HTTP server on a specific port.

### Step 7:
Run the Python script to serve web pages.

### Step 8:
Serve the HTML pages.

### Step 9:
Start the server script and check for errors.

### Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

## PROGRAM:
'''
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>

<head>
    <title>HTML Links</title>
</head>

<body>
    <p>Click on the following link</p>
    <a href="https://www.geeksforgeeks.org">
        GeeksforGeeks
    </a>
</body>

</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',80)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
'''


## OUTPUT:
![Screenshot 2025-03-18 104717](https://github.com/user-attachments/assets/52f5b359-a1e7-40ca-9180-cea625b3385e)

![Screenshot 2025-03-18 104731](https://github.com/user-attachments/assets/56238a4a-db08-479f-a939-b031dfab19f8)


## RESULT:
The program for implementing simple webserver is executed successfully.

