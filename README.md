# Docker Cheatsheet

## **Docker Basics**
Docker is a containerization platform that helps developers build, ship, and run applications efficiently.

---

## **Docker Installation & Version Check**
```sh
docker --version           # Check installed Docker version
docker info               # Display system-wide information
```

---

## **Working with Containers**
```sh
docker run <image>                      # Run a container from an image
docker run -d <image>                   # Run a container in detached mode
docker run --name <name> <image>        # Run with a custom name
docker run -p 8080:80 <image>           # Map ports from container to host
docker ps                               # List running containers
docker ps -a                            # List all containers
docker stop <container_id>              # Stop a running container
docker start <container_id>             # Start a stopped container
docker restart <container_id>           # Restart a container
docker rm <container_id>                # Remove a container
docker logs <container_id>              # View container logs
docker exec -it <container_id> bash     # Access a running container shell
```

---

## **Working with Images**
```sh
docker pull <image>                      # Pull an image from Docker Hub
docker images                            # List downloaded images
docker rmi <image_id>                    # Remove an image
docker tag <image> <new_tag>             # Tag an image
docker build -t <image_name> .           # Build an image from a Dockerfile
docker save -o <file>.tar <image_name>   # Save an image as a tar file
docker load -i <file>.tar                # Load an image from a tar file
```

---

## **Docker Networking**
```sh
docker network ls                       # List available networks
docker network create <network_name>    # Create a new network
docker network inspect <network_name>   # Inspect network details
docker network connect <network> <container>  # Connect a container to a network
docker network disconnect <network> <container>  # Disconnect a container
```

---

## **Docker Volumes**
```sh
docker volume ls                         # List all volumes
docker volume create <volume_name>       # Create a volume
docker volume inspect <volume_name>      # Inspect volume details
docker volume rm <volume_name>           # Remove a volume
docker run -v <volume_name>:/path <image>  # Mount a volume to a container
```

---

## **Docker Compose**
```sh
docker-compose up                        # Start services from docker-compose.yml
docker-compose up -d                     # Start services in detached mode
docker-compose down                      # Stop and remove services
docker-compose ps                        # List running services
docker-compose logs                      # View logs of services
```

---

## **Docker System Cleanup**
```sh
docker system prune                      # Remove unused data
docker image prune                       # Remove unused images
docker container prune                   # Remove stopped containers
docker volume prune                      # Remove unused volumes
```

---

## **Useful Docker Resources**
- [Docker Official Docs](https://docs.docker.com/)
- [Docker Hub](https://hub.docker.com/)
- [Docker Cheat Sheet](https://dockerlabs.collabnix.com/)

---

This cheatsheet provides quick references for managing Docker containers efficiently. Let me know if you have suggestions or improvements!
