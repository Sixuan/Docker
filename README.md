# Docker
Some useful docker related commands/dockerfile template

* Command to build a docker image via Dockerfile, -t specifies the image name "local.php" and tag "develop"
```
docker build -f Dockerfile -t local.php:develop .
```

* Command to run an image, -v mount the files stored in your local direcory /workspace/app to /var/www/app in the container
```
docker run -v /workspace/app:/var/www/app -p 5000:80 local.php:develop
```

* Get docker images
```
docker images
```

* Get running docker containers list
```
docker ps
```

* Force remove ALL the containers at once (regardless if they're running or not) 
```
docker rm -f $(docker ps -a -q)
```

* Clean up docker resouces
```
docker system prune
docker container prune
```

* Clean up docker resouces
```
docker pull blah.dkr.ecr.us-east-1.amazonaws.com/api:develop
```
