# FROM ubuntu:22.04
# RUN apt-get update
# RUN apt-get install -y nginx
# ADD . /var/www/html
# EXPOSE 80
# CMD ["nginx", "-g" , "daemon off;"]
#-----------------------------------

FROM node:18.12.1
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
RUN create-react-app lord
WORKDIR /lord
CMD npm start
# RUN npm start
