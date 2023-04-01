## Assignment 1:

Demonstrate minimum 15 basic docker command with explanation and screenshot.


### 1. Building the Docker Image:

```
docker build -t <image_name> .
```

Command is used to build the docker images. Create image using this directory's Dockerfile

![image](https://github.com/JyotiPandey111/Industry-Ready-Projects-Tasks/blob/bb60f34b4258015888f67c155d32fbe1403e59ac/dockercontent/building%20image.png)

### 2. Checking  the Docker Image Created:

```
docker image ls
```

Command is used to list all images that are locally stored with the Docker Engine.
![image](https://github.com/JyotiPandey111/Industry-Ready-Projects-Tasks/blob/dc96e5d92831d2597dc5a2a99a283316b5855da1/dockercontent/02%20list%20images.png)


### 3. Run the Docker Images:

```
docker run -d -p <host_port>:<container_port> <docker_image_name>
```

Command is used to run the docker images in detached mode. Run image host port to container port


![image](https://github.com/JyotiPandey111/Industry-Ready-Projects-Tasks/blob/43cbc17fc43d2cc317a8cb992825b51a4740c582/dockercontent/03%20run%20image.png)

### 4. Check the list of the Docker Container:

```
docker ps
```

Command is used to  see a list of all running containers

![image](https://github.com/JyotiPandey111/Industry-Ready-Projects-Tasks/blob/b9343fb28e1b7622e235e305068f01f1ce505f1a/dockercontent/04%20check%20containers.png)


### 5. Stop Docker Container:

```
docker stop <container_id>
```

Command is used to stop the specific container.


![image](https://github.com/JyotiPandey111/Industry-Ready-Projects-Tasks/blob/4311c9ac40d4b0c3efeab87f1c1dbbcce7954a92/dockercontent/05%20stop%20docker.png)


### 6. Delete the Container:

```
docker rm <hash> 
```
Command is used to remove the specified container from this machine


```
docker rm $(docker ps -a -q)

```
Command is used to remove all containers from this machine
clear



### 7. Delete Docker Image:

```
docker rmi <image_name>
```
or 
```
docker image rm <image_name>
```
Command is used to remove the specified image from this machine. Image will not delete if container is using its reference. so first delete the container then the respective image or delete the image forcefully mentioned in next commad.

![image](https://github.com/JyotiPandey111/Industry-Ready-Projects-Tasks/blob/015bcf7a4a8130c7c4ee866eb7336cfdb88defa7/dockercontent/06%20delete%20image.png)

```
docker rmi -f <image_name>
```
The above command is used to delete the image which has been refered by a container. we are deleteing the image forcefully. 


```
docker rmi $(docker images -q)
```
Command above will remove all images from this machine

![image](https://github.com/JyotiPandey111/Industry-Ready-Projects-Tasks/blob/37f1cdf801d6262d17e9a956724a7c4041bbdf16/dockercontent/07%20delete%20all%20image.png)




### 8. Push a image to a registry(DockerHub Account):

```
docker push <username>/<image_name>
```

Command is used to push the image to registry.

![image](https://github.com/JyotiPandey111/Industry-Ready-Projects-Tasks/blob/664e6419511faab3a5e717a99dcd78e9e25cfc0d/dockercontent/08%20push%20image%20.png)


### 9. Pull a image from the registry(DockerHub Account):


Command is used to pull the image from registry.
Copy the pull command
![Image](https://github.com/JyotiPandey111/Industry-Ready-Projects-Tasks/blob/18ac503e042798576452c98b281771532d4b295e/dockercontent/pull%20image.png)

Pull the command
![Image](https://github.com/JyotiPandey111/Industry-Ready-Projects-Tasks/blob/18ac503e042798576452c98b281771532d4b295e/dockercontent/pull%20image%202.png)

Run the Image locally.
![Image](https://github.com/JyotiPandey111/Industry-Ready-Projects-Tasks/blob/f4f6b5ce7576cee4d07e6fb566f4283853ed6c70/dockercontent/run%20command.png)
![Image](https://github.com/JyotiPandey111/Industry-Ready-Projects-Tasks/blob/b62d4c60820bcbab1d72284aa4b18d4e93349194/dockercontent/run.png)

