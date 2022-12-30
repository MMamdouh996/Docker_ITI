# Problem 2
## Create react app docker container "using single stage, Multi-Stage Dockerfile"
---
---
# Still didn't do the multi stage
```Docker
FROM node:18.12.1 AS buildalias
RUN apt-get update
#installing nodejs ( it should include npm by default)
RUN apt-get install -y nodejs
#just checking for node version
RUN node -v 
#updating npm with specific version (( docker container note ))
RUN npm install -g npm@9.2.0
#to install "create-react-app" command we must install it with npm 
# i standsfor install 
# -g standsfor globally 
RUN npm i -g create-react-app
#to create react app we run "create-react-app <app_name>"
RUN create-react-app fanapp
WORKDIR /fanapp
RUN ls
# CMD npm start
# CMD [ "npm","start" ]
# the line below will run the app and put it inside dir called build
# RUN npm run fanapp
# RUN npm start

FROM nginx:alpine
COPY --from=buildalias /fanapp /usr/share/nginx/html
EXPOSE 80
ENTRYPOINT [ "nginx" , "-g" , "daemon off;" ]
```
---
---
# Dockerfile
```Docker
FROM node:18.12.1
RUN apt-get update
#installing nodejs ( it should include npm by default)
#RUN apt-get install -y nodejs
#just checking for node version
#RUN node -v
#updating npm with specific version (( docker container note ))
RUN npm install -g npm@9.2.0
#to install "create-react-app" command we must install it with npm 
# i standsfor install 
# -g standsfor globally 
RUN npm i -g create-react-app
#to create react app we run "create-react-app <app_name>"
RUN create-react-app lord
WORKDIR /lord
#CMD npm start

```

```bash
$sudo docker build -t node:cr8reactapp .
$ sudo docker run -it -d -p 3500:3000 node:cr8reactapp #now we can access it throgh localhost@3500
```

