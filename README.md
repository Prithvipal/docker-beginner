# docker-beginner

## Commands

1. `docker run centos`
2. `docker run -d centos` // to run in detached mode
3. `docker attach <container_id>` // to attach terminal to container again. When you run Ctrl+c, it will stop the container as well.
4. `docker run -it centos bash` // to exec into the container while run container.
5. `docker ps` // lists all the containers
6. `docker ps -a` // lists all the containers including exited ones.
7. `docker rm <container_id>` // to remove container. It will only remove exited container.
8. `docker stop <container_id or contaniner_name>` // stops container running container
9. `docker start <container_id or contaniner_name>` // start container stoped container
10. `docker images` or `docker image ls` // lists all the images
11. `docker rmi ubuntu` or `docker image rm ubuntu` // removes image. It only remove image if it is not used in any container including exited onces.
12. `docker pull` //pull image without running the container.
13. `docker run ubuntu sleep 20` // run contaier and sleeps for 20 seconds
14. `docker exec <container_id> cat /etc/*release*` // runs cat command into the container.
15. `docker run -p 82:5000 kodekloud/webapp` // maps port 82 of local machine to 5000 of container
16. `docker run -v /opt/datadir:/var/lib/mysql mysql` // attaches volume /opt/datadir of local machine to /var/lib/mysql of container
17. `docker inspect <container_id or container_name>` // to see details of container
18. `docker logs -f <container_id or container_name>` // to see logs of the container
19. `docker create volume data_vol` // creates a new volume. It is called volume mount.
20. `docker run -v data_vol:/var/lib/mysql mysql` // creates new container from mysql image and attach newly created volume. Plesae note that if volume specified in this command is not create in advance, the run command will create a new volume and attach it to the container.
21. `docker volume ls` // lists all the volumes
22. `docker run -v /data/mysql:/var/lib/mysql mysql` // mount to given local storage instead of default volume path. It is called bind mount.
23. `docker run --mount type=bind,source=/data/mysql,target=/var/lib/mysql mysql` // a new way to mount the volume.
24. `docker run -it --privileged --pid=host debian nsenter -t 1 -m -u -n -i sh` // exec into docker host and you can see all docker directories in /var/lib/docker
25. `docker systen df` // to check space consumed by docker resources. i.e container, images etc.
26. `docker system df -v ` // to check space consumed by docker resources. i.e container, images etc. it shows in details of each type.


