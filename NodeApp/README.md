# Node APP ready to be Dockerized

## Build the image:
```
docker build . -t <your username>/node-web-app
```
## Run the image:
```
docker run -p 49160:3000 -d <your username>/node-web-app
```
## GET Request in the terminal:
```
$ curl -i localhost:49160

HTTP/1.1 200 OK
X-Powered-By: Express
Content-Type: text/html; charset=utf-8
Content-Length: 12
ETag: W/"c-M6tWOb/Y57lesdjQuHeB1P/qTV0"
Date: Mon, 13 Nov 2017 20:53:59 GMT
Connection: keep-alive

Hello world
```