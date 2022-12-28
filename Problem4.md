Problem 4

• Run the image httpd again without attaching any volumes
• Add html static files to the container and make sure they are accessible
• Commit the container with image name my apache
• Create a dockerfile for ngnix and build the image from this dockerfile

```bash
$ sudo docker run -it --name nginx3 nginx bash
root@37fb442f6244:/# cd /var/www
root@37fb442f6244:/var/www# echo testting >> testfile.html
root@37fb442f6244:/var/www# exit

$ sudo docker commit e31 myimage:justAcomment
$ sudo docker run myimage:justAcomment -it -p 8099:80 --name nginx45 nginx bash

root@58f4c7b50419:/# cd usr/share/nginx/html/
root@58f4c7b50419:/usr/share/nginx/html# ls
50x.html  index.html  testfile.html

```
---

