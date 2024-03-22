# EX01 Developing a Simple Webserver

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

```C

from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<html>
      <title>top 5 software industries</title>
      <body>
             <table border="2" cellspacing="10" cellpaddding="6">
                     <caption> Top 5 Revenue Generating Software Companies </caption>
                     <tr>
<th>s.no</th>
<th>companies</th>
<th>revenue</th> 
</tr>  
<tr> 
<th>1</th>
<th>Microsoft</th>
<th>65 billion</th>
</tr>
<tr>
<th>2</th>
<th>oracle</th>
<th>29.5 billon</th>
</tr>
<tr>
<th>3</th>
<th>IBM </th>
<th>29.1 billon</th>
</tr>
<tr>
<th>4</th>
<th>SAP</th>
<th>6.4 billon</yh>
</tr>
<tr>
<th>5</th>
<th>symentec</th>
<th>5.6 billion</th>
</boby>
</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```

## OUTPUT:
![1](https://github.com/indrajasukumar/simplewebserver/assets/145115195/14946870-e097-42cd-8aa5-80b45eb1f5ab)
![2](https://github.com/indrajasukumar/simplewebserver/assets/145115195/5d435419-c487-4830-bc28-d092b3660b31)

## RESULT:
The program for implementing simple webserver is executed successfully.
