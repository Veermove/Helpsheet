# Docker clean-up

## List all containers

```
$ docker ps [OPTIONS]
```
Show running containers:
```
$ docker ps
```

Useful flags: 
```
$ docker ps -a  => shows all containers
$ docker ps -q  => show only container ID
```

## Start / Stop

Respectivly starts and stops containers:
```
$ docker start my_container
$ docker stop my_container
```

Stop **all** containers:
```
$ docker stop $(docker ps -q)
```

## Remove containers

Remove container:

```
$ docker rm my_container
```

Remove **all** containers (all containers must be stopped beforehand):
```
$ docker rm $(docker ps -a -q)
```

# Docker-compose

## Up
Create and start containers:
```
$ docker-compose up
```

Builds, (re)creates, starts, and attaches to containers for a service.

Unless they are already running, this command also starts any linked services.

### -d
```
$ docker-compose up -d
```
Adds Detached mode: Run containers in the background,
print new container names.

## Down
Stops containers and removes containers, networks, volumes, and images created by `up`:
```
docker-compose down
```

## Start/stop
Respectivly starts and stops services:
```
$ docker-compose start
$ docker-compose stop
```





