# docker-beginner

## Commands

1. docker run centos
2. docker run -d centos // to run in detached mode
3. docker attach 759ae3 // to attach terminal to container again. When you run Ctrl+c, it will stop the container as well.
4. docker run -it centos bash // to exec into the container while run container.
5. docker ps // lists all the containers
6. docker ps -a // lists all the containers including exited ones.
7. docker rm <container_id> // to remove container. It will only remove exited container.
8. docker stop <container_id or contaniner_name>