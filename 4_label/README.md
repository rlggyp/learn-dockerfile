### Building the Docker Image
To build the Docker image, use the following command format:  
`docker build -t <image_name>:<tag> .`  
```bash
docker build -t hello_world:label .
```
### Creating a Container
You can create a container using the image that has been built with the following command:
```bash
# This command creates a container, allows you to enter it interactively, and removes the container when you exit.
docker run -it --rm hello_world:label bash
```
