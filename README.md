# Helpful Docker Commands For Developers To Know

| Command                                                                 | Usage | Freq |
|:----------------------------------------------------------------------- | :---- | :--- |
| `docker container ls -a`                                                | list all running containers | :heavy_check_mark: |
| `docker container rm <container id1> <container id1>`                   | remove specific container(s) | :heavy_check_mark: |
| `docker container ls -a --filter status=exited --filter status=created` | remove exited containers |  |
| `docker container prune --filter "until=12h"`                           | remove all images that are created more than 12 hours ago | :heavy_check_mark: |
| `docker container stop $(docker container ls -aq)`                      | stop all running containers | :heavy_check_mark: |
| `docker container rm $(docker container ls -aq)`                        | remove all running containers | :heavy_check_mark: |
| `docker stop $(docker ps -aq)`                                          | stop all running containers | :heavy_check_mark: |
| `docker rm $(docker ps -aq)`                                            | remove all running containers | :heavy_check_mark: |
| `docker system prune`                                                   | remove all stopped containers, all dangling images, and all unused networks. Use -f or -force to bypass the prompt | :heavy_check_mark: |
| `docker system prune --volumes`                                         | remove all unused volumes |  |
| `docker image ls`                                                       | list all images |  |
| `docker image rm <image id1> <image id2>`                               | remove specific images | :heavy_check_mark: |
| `docker rmi $(docker images -aq)`                                       | remove all images | :heavy_check_mark: |
| `docker image prune [-f, -force]`                                       | remove dangling images |  |
| `docker image prune -a`                                                 | remove all unused images |  |
| `docker image prune -a --filter "until=12h"`                            | remove all images that are created more than 12 hours ago |  |
| `docker volume ls`                                                      | list all volumes |  |
| `docker volume rm <volume name>`                                        | remove volume |  |
| `docker volume prune`                                                   | remove all unused volumes |  |
| `docker network ls`                                                     | list all networks |  |
| `docker network rm <network id>`                                        | remove one or more networks |  |
| `docker network prune`                                                  | remove all unused network |  |
