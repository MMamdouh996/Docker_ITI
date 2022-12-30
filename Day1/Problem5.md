Problem 5

•Create a volume called mysql_data, then deploy a MySQL database called app-database.
Use the mysql latest image, and use the -e flag to set MYSQL_ROOT_PASSWORD to P4sSw0rd0!
.Mount the mysql_data volume to /var/lib/mysql.
The container should run in the background.

```bash

$ sudo docker run -it -d -v ~/mysql_data:/var/lib/mysql --name app-database -e MYSQL_ROOT_PASSWORD=123123123 mysql:latest
```
---

