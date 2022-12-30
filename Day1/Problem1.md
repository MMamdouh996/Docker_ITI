# Problem 1
### 1. Run the container hello-world
```bash
$ sudo docker run hello-world
```

### 2. Check the container state
```bash
$ sudo docker ps -a
```

### 3. start the stopped container
```bash
$ sudo docker ps -a
$ sudo docker start ebad #ebad is the id of the container
```

### 4. remove the container
```bash
$ sudo docker rm ebad #ebad is the id of the container
```

### 5. remove the image
```bash
$ sudo docker image ls
$ sudo docker rmi feb5 #feb5 is the id of the image
unable to delete feb5d9fea6a5 (must be forced) - image is being used by stopped container bd3749c25f30
$ sudo docker rm bd37
$ sudo docker rmi feb5
$ sudo docker image ls

```

