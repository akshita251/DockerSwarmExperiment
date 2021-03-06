# DockerSwarmExperiment
Set up a cluster with single host

## Initializing Docker swarm

```bash
$ docker swarm init
```
## Running the service

Use the Compose file to start up our application stack in Swarm.

```bash
$ docker stack deploy nodeapp -c docker-compose.yml
```

## Scaling of services

We used the docker service scale command to start more replicas of our service.

```bash
$ docker service scale nodeapp_web=4
```

We can check our service status by using the command mention above, 

```bash
$ docker service ls
```

## Removing the stack and closing swarm

```bash
$ docker stack rm nodeapp
$ docker swarm leave --force
```
## Access the application

#### Returrns container id
http://localhost:9090

#### Visualizer
http://localhost:8080