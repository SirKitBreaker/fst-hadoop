# Hadoop Classroom Environment
The official training environment for our Hadoop classes.

## Prerequisite Tools
* Docker

## Instructions for Use
### Using Our Pre-Built Image ( Recommended )
Our pre-built image is available at: `registry.gitlab.com/training-support/training-environments:hadoop-v1`

The full command to run the container is:
```bash
$ docker container run -it \
  -p 9870:9870 \
  -p 8088:8088 \
  registry.gitlab.com/training-support/training-environments:hadoop-v1 \
  bash
```

This will drop you at a bash shell where you can interact with the running container.

#### Important Note
This container is ephemeral, and not really intended to be used with volumes.
If you need to keep it running in the background for an extended amount of time, then launch the container in detached mode and connect to it with `docker exec -it $CONTAINER_ID bash`

### Building the Image ( Optional )
1. Clone the Repo
2. Clone this Directory
3. Run `docker build .` to generate the image. Feel free to tag it if you need to.
