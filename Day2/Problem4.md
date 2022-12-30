# Problem 4

## Step 1 Create your bridge network
```bash
$sudo docker network create mybridge
```

## Step 2 two containers from ubuntu image with different names 
### Dockerfile

```Docker
FROM ubuntu:22.04
RUN apt-get update
RUN apt-get install -y nginx
#to add ping command
RUN apt-get install iputils-ping
EXPOSE 80
CMD ["nginx", "-g" , "daemon off;"]
```

```bash
$sudo docker build -t ubuntu:mybridge
$sudo docker run --network mybridge --name u1 -p 8050:80 ubuntu:mybridge # The mapping is not necessary 
$sudo docker run --network mybridge --name u2 -p 8040:80 ubuntu:mybridge # The mapping is not necessary 

```
## Step 3 and try to ping each other using NAME.
```bash
$sudo docker exec -ti u1 ping u2
```
