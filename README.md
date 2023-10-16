# EX01 Developing a Simple Webserver

## Date: 11.10.2023

## AIM:

To develop a simple webserver to serve html pages.

## DESIGN STEPS:

### Step 1: 

HTML content creation.

### Step 2:

Design of webserver workflow.

### Step 3:

Implementation using Python code.

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver.

## PROGRAM:
```
## Developed by:S.A.Amrutha
## Reg no:212222110004

from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<title>My webserver</title>
</head>
<body>
<h1><u>Languages used iun Web Development</u><h1>
<ul>
<li>HTML</li>
<li>CSS</li>
<li>JavaScript</li>
<li>Bootstrap</li>
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
```
## OUTPUT:

![expt 1 (1)](https://github.com/amrutha23ashok/simplewebserver/assets/120772913/be6e4699-91e5-4c15-9480-101b068eb839)

![expt 1 (2)](https://github.com/amrutha23ashok/simplewebserver/assets/120772913/a3b70166-be40-4dab-adcd-d6ddcbc79ac4)

## RESULT:

The program for implementing simple webserver is executed successfully.
