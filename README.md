# ionic-interactive-dockercontainer
This a Dockerfile that creates a dockercontainer that is all you need when developing ionic apps. just start the container detached  with your file system mounted and execute bash and do all you development in the container. 

## Getting started
1. download repo 
2. docker build -t ionic-interactive .
3. create a folder where you want to have your ionic projects and cd into it


## Run without docker-compose
```
$ docker run -ti --rm --user=docker --net host --privileged -v /dev/bus/usb:/dev/bus/usb -v $(pwd):/App:rw ionic-interactive bash
```

## Run with docker-compose.
```
$ docker-compose up -d
$ docker exec -it ionic-interactive_front_1 bash (start new tabs and do this as many times as you like if you want to run multiple things, like grunt watch, ionic serve etc.)
```

