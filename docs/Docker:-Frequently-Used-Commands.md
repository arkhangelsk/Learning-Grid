**Check version of docker installation:**
```
docker --version
docker-compose --version
docker-machine --version
```

**Check if your docker installation is working:**
```
docker run hello-world
```
**View the list of running containers:**

```
docker container ls
```
or 
```
docker ps
```

**View the list of all (running & stopped) containers:**
```
docker container ls -a
```

**Stop Container:**
```
docker container stop container-name
```

**Remove Container:**
```
docker container rm container-name
```

**List docker images:**
```
docker image ls
```

**Remove docker image:**
```
docker image rm image-repository
```

**Search docker repository for your desired container:**
```
docker search puppeteer
```