## Dockerize an app

```console
docker build -t fastapi-image .
docker run --name fastapi-container -p 80:80 fastapi-image
docker run -d --name fastapi-container -p 80:80 fastapi-image
```
## Immediate file changes (volumes)

```console
 docker stop fastapi-container
 docker ps -a
 docker rm fastapi-container

 docker run -d --name fastapi-container -p 80:80 -v $(pwd):/code fastapi-image
 ```