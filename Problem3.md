Problem 3

• Run a container httpd with name apache and attach a volume to the container
• Volume for containing static html file
•Run a new container with the following:
• Attach the volume that was attached to the
previous container
• Map port 80 to port 9898 on you host machine
• Access the html files from your browser


```bash
$ sudo docker run -it -v ~vol:/var/www --name nginx3 nginx bash
root@37fb442f6244:/# cd /var/www
root@37fb442f6244:/var/www# echo testting >> test.html
root@37fb442f6244:/var/www# exit
$ sudo docker rm r4r 
$ sudo docker run -it -v ~vol:/usr/share/nginx/html -p 8099:80 --name nginx4 nginx bash
root@31fb243f6255:/# cd /usr/share/nginx/html
root@31fb243f6255://usr/share/nginx/html/# ls
test.html
root@31fb243f6255:/usr/share/nginx/html/# service nginx start
root@31fb243f6255:/usr/share/nginx/html/# service nginx status
nginx is running.
#now we can connect to the localhost:8099/test.html
```
---

