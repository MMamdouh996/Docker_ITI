# FROM ubuntu:22.04
# RUN apt-get update
# RUN apt-get install -y nginx
# ADD . /var/www/html
# EXPOSE 80
# CMD ["nginx", "-g" , "daemon off;"]

FROM node:18.12.1
RUN apt-get update
RUN apt-get install -y nodejs
# RUN apt-get install -y npm
# RUN npm install tar@6 -g
RUN node -v
# RUN npm install tar@latest
RUN npm install -g npm@9.2.0
RUN npm i -g create-react-app
#to create react app we run "create-react-app <app_name>"
RUN create-react-app lord

