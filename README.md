# Name:Ramya P
# Register number:212223240137
# Date:
#               EX01 Developing a Simple Webserver 
# AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

# DESIGN STEPS:
## Step 1:
HTML content creation.

## Step 2:
Design of webserver workflow.

## Step 3:
Implementation using Python code.

## Step 4:
Serving the HTML pages.

## Step 5:
Testing the webserver.

# PROGRAM:
```
import http.server
import socketserver

PORT = 8000

class MyHandler(http.server.SimpleHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header("Content-type", "text/html")
        self.end_headers()
        self.wfile.write(b"<html><body><h1>Hi Hello</h1></body></html>")

with socketserver.TCPServer(("", PORT), MyHandler) as httpd:
    print(f"Serving at port {PORT}")
    httpd.serve_forever()
```

# OUTPUT:
![Screenshot 2025-03-17 082935](https://github.com/user-attachments/assets/c37d15b8-6afe-4e4b-87dd-395474b9516d)

# RESULT:
The program for implementing simple webserver is executed successfully.
