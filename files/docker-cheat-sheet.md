# Docker Cheat Sheet (for IoT Edge)

([Previous](../README.md))

- `docker login -u <username> -p <password> <container_registry_name>.azurecr.io`

--------

- `docker build -t <image>:<tag> .` build an image in the current respository

--------

- `docker run -d <image>` run image detached image (in the background)
- `docker run -it <image>` run image /bin/bash (directly in terminal)
- `docker run -p <host_port>:<container_port> <image>` bind ports 
- `docker run -v <host_path>:<container_path> <image>` bind a volume (and create it if not existing)

-------------

- `docker exec -i -t <container_name> /bin/bash` execute bash for a running container

-------------

- `docker ps` display all running containers
- `docker ps -a ` display all containers
- `docker images` display all images

-------------

- `docker logs <edge_module_name>` display logs of an edge module container

----------

- `docker rmi -f <imageId> <imageId2> <...>` remove images by id (*force*)
- `docker system prune` remove all useless images, containers or volumes  
