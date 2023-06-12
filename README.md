# Docker Run

Format:

`docker run image_name:tag_name "command`

`docker run ubuntu cat /etc/*release*`

If you don't specify any tag, in that case docker assumes the you want to run/pull the latest tag.

`docker run ubuntu:17.10 cat /etc/*release*`

### Running docker container in dettached mode:

`docker run -d ubuntu sleep 100`

### Attach docker container:
`docker attach "container id"`

### Access docker container using internal IP:
`docker inspect "container id"` (to find the internal IP of the docker container)

## Access docker container externally: (Port Mapping)

`docker run -p host_port:container_port image_name`

`docker run -p 8080:8080 ubuntu`

## Volumne Mapping:

`docker run -v host_dir:container_dir -u username`

`docker run -v /root/my_jenkins_data:/var/jenkings_home -u root jenkins`

### Port and Volume Mapping:

`docker run -p 8080:8080 -v /root/my_jenkins_data:/var/jenkings_home -u root jenkins`


# Docker Image:

DOCKER FILE

Structure of docker fike

| INSTRUCTION | ARGUMENT |

