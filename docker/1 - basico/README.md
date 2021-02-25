` docker build -t app:v1 .`

`docker run -d -p 5000:5000 app:v1`

```
curl localhost:5000
Hello World!!
```

```
docker image ls
REPOSITORY   TAG       IMAGE ID       CREATED          SIZE
app          v1        29328ba86b76   23 minutes ago   893MB
python       3.8       8f6adb7689b5   9 days ago       883MB
```

`docker build -f Dockerfile2 -t app:v2 .`

`docker run -d -p 5001:5000 app:v2`

```
curl localhost:5000
Hello World!!
```

```
docker image ls
REPOSITORY   TAG       IMAGE ID       CREATED          SIZE
app          v1        29328ba86b76   23 minutes ago   893MB
python       3.8       8f6adb7689b5   9 days ago       883MB
