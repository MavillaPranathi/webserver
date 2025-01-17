# Developing a Simple Webserver

# AIM:

To develop a simple webserver to display top five programming languages.

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
```
from http.server import HTTPServer,BaseHTTPRequestHandler
content="""
<!DOCTYPE html>
<html>
<head>
<title>My webserver</title>
</head>
<body>
<h1>TOP FIVE WEB APPLICATION DEVELOPMENT</h1>
<h2> hello </h2>
<h2>1.Django</h2>
<h2>2.Angular</h2>
<h2>3.Ruby on Rails</h2>
<h2>4.React</h2>
<h2>5.Bootstrap</h2>
</body>
</html>
"""
class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200)
        self.send_header('content-type','text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
print("This is my webserver")
server_address=('',80)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
```

## OUTPUT:
![webserver pranathi](https://user-images.githubusercontent.com/118343610/214346989-bc772f26-b298-4e80-ad08-9d997d96f9d7.jpeg)

![webss pranathi](https://user-images.githubusercontent.com/118343610/214347020-3341f4a5-fa42-4d46-b4fd-0b76d7357059.jpeg)


## RESULT:
The program is executed succesfully

