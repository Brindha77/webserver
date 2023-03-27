# Developing a Simple Webserver

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:

DEVELOPED BY : BRINDHA R

REGISTER NO : 22008265

```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<title>My webserver</title>
</head>
<body>
<h1><u>Top five web application development frameworks.</u><h1>
<ul>
<li>Django</li>
<li>Angular or Angular JS</li>
<li>Laravel.</li>
<li>Meteor. </li>
<li>ASP.NET. </li>
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

![Screenshot from 2023-03-27 14-00-39](https://user-images.githubusercontent.com/118889143/227886987-ab277c05-113a-4ee4-87a1-0e8bb2740b7d.png)


## RESULT:
The program is executed succesfully.
