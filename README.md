# Docker : NGINX Example

## Requirements
- docker

## How to

Download nginx:alpine image
```
docker pull nginx:alpine
```
Run it!

```
docker-compose up
```

## What can I see?

If you call for the load-balancer in tcp800 port, you'll see webserver1 and webserver2 alternating to reply your call: 
```
curl localhost:800
    Hello World from webserver1!

curl localhost:800
    Hello World from webserver2!
```
- WebServer1 and WebServer2 are configured to serve all requests (http - tcp/80) with a static hello world page.
- Load-balancer is configured to server all requests (http - tcp/80) redirecting traffing to webserver1 or webserver2 (round robin method).