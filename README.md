# cassandra

[![](https://imagelayers.io/badge/openkbs/cassandra:latest.svg)](https://imagelayers.io/?images=openkbs/cassandra:latest 'Get your own badge on imagelayers.io')

##Components:
- ref: https://github.com/davidshen84/docker-cassandra-learn
- ref: https://github.com/davidshen84/docker-jupyter

## Pull the image from Docker Repository

```bash
docker pull openkbs/cassandra
```
## Connect to cassandra Docker
host/port=> 0.0.0.0:18888 
login/passwd=> (see above)

## Base the image to build add-on components

```Dockerfile
FROM openkbs/cassandra
```

## Run the image

Then, you're ready to run:
- make sure you create your work directory, e.g., ./data

```bash
mkdir ./data
docker run -d --name my-cassandra -p 18888:8888 openkbs/cassandra
```

## Build and Run your own image
Say, you will build the image "my/cassandra".

```bash
docker build -t my/cassandra .
```

To run your own image, say, with some-cassandra:

```bash
mkdir ./data
docker run -d --name some-cassandra -p 18888:88882 my/cassandra
```

## Shell into the Docker instance

```bash
docker exec -it some-cassandra /bin/bash
```


