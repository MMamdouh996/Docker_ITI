# Problem 1
## Create your own nginx docker image based on ubuntu “NEVER USE FROM nginx”
### Install nginx
### Two index.html one as file and another as .tar "/var/www/html"
### Expose
### Start
### Port mapping

Dockerfile
```Docker
FROM ubuntu:22.04
RUN apt-get update
RUN apt-get install -y nginx
ADD . /var/www/html
EXPOSE 80
CMD ["nginx", "-g" , "daemon off;"]
```

```bash
$ sudo docker build -t ubuntu:22.04nX .
$ sudo docker run -it -p 8099:80 ubuntu:22.04nX #i can access localhost:8099 from my local machine now
```

