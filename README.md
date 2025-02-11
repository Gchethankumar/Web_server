# Developing a Simple Webserver

# AIM:

Develope a webserver to display about top five web application development frameworks.


# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver

# PROGRAM:
``` python html 
Developed by: G.Chethan kumar
Reference.No.: 22005596
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
</head>
</head>
<body>
<h1>WELCOME</h1>
<h2>NAME:G CHETHAN KUMAR</h2>
<h2>REF.NO.:22005596</h2>
<h3>LIST OF FRAMEWORKS</h3>
<h4>-Django</h4>
<h4>-Ruby on Rails</h4>
<h4>-Angular</h4>
<h4>-Meteor</h4>
<h4>-jQuery</h4>
</body>
</html>
"""

class Hellohandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type','text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',80)
httpd = HTTPServer(server_address, Hellohandler)
httpd.serve_forever()
```
# OUTPUT:
![mywebserver1](https://user-images.githubusercontent.com/118348224/210048524-79df41d9-9277-4ebd-a044-664d4a9ff712.png)


# RESULT:

The program is executed succesfully.
