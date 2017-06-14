Create Docker Image
docker build -t <image_name> <dir_with_Dockerfile>

Listing Docker Images
`docker images` 

List Running Containers
`docker ps`

List All Containers (not deleted)
`docker ps -a`

-q Container_IDs only
-l Latest Entry

Create Container with BASH shell with one exposed port
`docker create -p <container_port>:<host_port> -i -t <image_repository> /bin/bash

List port mapping between container and the host ports
docker port <container_id>

Start and Attach to Container
`docker start -a -i <container_ID>

Delete Docker Container
`docker rm <container_id>

Delete Docker Image
`docker rmi <image_id>`
