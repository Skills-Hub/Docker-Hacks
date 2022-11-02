## Docker 
Fast, consistent delivery of your applications
Docker streamlines the development lifecycle by allowing developers to work in standardized environments using local containers which provide your applications and services. Containers are great for continuous integration and continuous delivery (CI/CD) workflows.


### Install Docker
### Commands
### Labs
### Run
### Environment Variables
### Images
### CMD vs ENTRYPOINT
### Networking
### Storage
### Compose
### Registry
### Engine
### Docker on Windows
### Docker on Mac
### Container Orchestration
### Docker Swarm




### 1. What is Docker?

Docker is Open Source software. It provides the automation of Linux application deployment in a software container.

We can do operating system level virtualization on Linux with Docker.


Docker can package software in a complete file system that contains software code, runtime environment, system tools, & libraries that are required to install and run the software on a server.

###  2. What is the difference between Docker image and Docker container?

Docker container is simply an instance of Docker image.


A Docker image is an immutable file, which is a snapshot of container. We create an image with build command.

When we use run command, an Image will produce a container.

In programming language, an Image is a Class and a Container is an instance of the class.

### 3. How will you remove an image from Docker?

We can use docker rmi command to delete an image from our local system.

Exact command is:

% docker rmi <Image Id>


If we want to find IDs of all the Docker images in our local system, we can user docker images command.

% docker images

If we want to remove a docker container then we use docker rm command.

% docker rm <Container Id>

### 4.    How is a Docker container different from a hypervisor?

In a Hypervisor environment we first create a Virtual Machine and then install an Operating System on it. After that we deploy the application. The virtual machine may also be installed on different hardware configurations.

In a Docker environment, we just deploy the application in Docker. There is no OS layer in this environment. We specify libraries, and rest of the kernel is provided by Docker engine.

In a way, Docker container and hypervisor are complementary to each other.

### 5.Can we write compose file in json file instead of yaml?

Yes. Yaml format is a superset of json format. Therefore any json file is also a valid Yaml file.

If we use a json file then we have to specify in docker command that we are using a json file as follows:

% docker-compose -f docker-compose.json up

### 6.Can we run multiple apps on one server with Docker?

Yes, theoretically we can run multiples apps on one Docker server. But in practice, it is better to run different components on separate containers.


With this we get cleaner environment and it can be used for multiple uses.

### 7.What are the common use cases of Docker?

Some of the common use cases of Docker are as follows:

Setting up Development Environment:We can use Docker to set the development environment with the applications on which our code is dependent.
Testing Automation Setup: Docker can also help in creating the Testing Automation setup. We can setup different services and apps with Docker to create the automation testing environment.
Production Deployment: Docker also helps in implementing the Production deployment for an application. We can use it to create the exact environment and process that will be used for doing the production deployment.
### 8.What are the main features of Docker-compose?

Some of the main features of Docker-compose are as follows:

Multiple environments on same Host: We can use it to create multiple environments on the same host server.
Preserve Volume Data on Container Creation: Docker compose also preserves the volume data when we create a container.
Recreate the changed Containers: We can also use compose to recreate the changed containers.
Variables in Compose file: Docker compose also supports variables in compose file. In this way we can create variations of our containers.

### 9. What is the most popular use of Docker?

The most popular use of Docker is in build pipeline. With the use of Docker it is much easier to automate the development to deployment process in build pipeline.

We use Docker for the complete build flow from development work, test run and deployment to production environment.

### 10. What is the role of open source development in the popularity of Docker?

Since Linux was an open source operating system, it opened new opportunities for developers who want to contribute to open source systems.

One of the very good outcomes of open source software is Docker. It has very powerful features.

Docker has wide acceptance due to its usability as well as its open source approach of integrating with different systems.

### 11.  What is the difference between Docker commands: up, run and start?

We have up and start commands in docker-compose. The run command is in docker.

Up: We use this command to build, create, start or restart all the services in a docker-compose.yml file. It also attaches to containers for a service. This command can also start linked services.
Run:  We use this command for adhoc requests. It just starts the service that we specifically want to start. We generally use it run specific tests or any administrative tasks.
Start: This command is used to start the container that were previously created but are not currently running. This command does not create new containers.

### 12. What is Docker Swarm?

Docker Swarm is used to create a cluster environment. It can turn a group of Docker engines into a Single virtual Docker Engine. This creates a system with pooled resources. We can use Docker Swarm to scale our application.

### 13. What are the features of Docker Swarm?

Some of the key features of Docker Swarm are as follows:

Compatible: Docker Swarm is compatible with standard Docker API.
High Scalability: Swarm can scale up to as much as 1000 nodes and 50000 containers. There is almost no performance degradation at this scale in Docker Swarm.
Networking: Swarm comes with support for Docker Networking. High
Availability: We can create a highly available system with Docker Swarm. It allows use to create multiple master nodes so that in case of a failure, another node can take over.
Node Discovery: In Docker Swarm, we can add more nodes and the new nodes can be found with any discovery service like etcd or zookeeper etc.

### 14. What is a Docker Image?

Docker Image is the blue print that is used to create a Docker Container. Whenever we want to run a container we have to specify the image that we want to run.

There are many Docker images available online for standard software. We can use these images directly from the source.

The standard set of Docker Images is stored in Docker Hub Registry. We can download these from this location and use it in our environment.

We can also create our own Docker Image with the software that we want to run as a container.

### 15. What is a Docker Container?

A Docker Container is a lightweight system that can be run on a Linux operating system or a virtual machine. It is a package of an application and related dependencies that can be run independently.

Since Docker Container is very lightweight, multiple containers can be run simultaneously on a single server or virtual machine.

With a Docker Container we can create an isolated system with restricted services and processes. A Container has private view of the operating system. It has its own process ID space, file system, and network interface.

Multiple Docker Containers can share same Kernel.

### 16. What is Docker Machine?

We can use Docker Machine to install Docker Engine on virtual hosts. It also provides commands to manage virtual hosts.

Some of the popular Docker machine commands enable us to start, stop, inspect and restart a managed host.

Docker Machine provides a Command Line Interface (CLI), which is very useful in managing multiple hosts.

### 17. Why do we use Docker Machine?

There are two main uses of Docker Machine:

Old Desktop: If we have an old desktop and we want to run Docker then we use Docker Machine to run Docker. It is like installing a virtual machine on an old hardware system to run Docker engine.
Remote Hosts: Docker Machine is also used to provision Docker hosts on remote systems. By using Docker Machine you can install Docker Engine on remote hosts and configure clients on them.

### 18. How will you create a Container in Docker?

To create a Container in Docker we have to create a Docker Image. We can also use an existing Image from Docker Hub Registry.

We can run an Image to create the container.

### 19. Do you think Docker is Application-centric or Machine-centric?

Docker is an Application-centric solution. It is optimized for deployment of an application. It does not replace a machine by creating a virtual machine. Rather, it focuses on providing ease of use features to run an application.

### 20. Can we lose our data when a Docker Container exits?

A Docker Container has its own file-system. In an application running on Docker Container we can write to this file-system. When the container exits, data written to file-system still remains. When we restart the container, same data can be accessed again.

Only when we delete the container, related data will be deleted.

### 21. Can we run more than one process in a Docker container?

Yes, a Docker Container can provide process management that can be used to run multiple processes. There are process supervisors like runit, s6, daemontools etc that can be used to fork additional processes in a Docker container.

### 22.    What are the objects created by Docker Cloud  in Amazon Web Services (AWS) EC2?

Docker Cloud creates following objects in AWS EC2 instance:

VPC: Docker Cloud creates a Virtual Private Cloud with the tag name dc-vpc. It also creates Class Less Inter-Domain Routing (CIDR) with the range of 10.78.0.0/16.
Subnet: Docker Cloud creates a subnet in each Availability Zone (AZ). In Docker Cloud, each subnet is tagged with dc-subnet.
Internet Gateway: Docker Cloud also creates an internet gateway with name dc-gateway and attaches it to the VPC created earlier.
Routing Table: Docker Cloud also creates a routing table named dc-route-table in Virtual Private Cloud. In this Routing Table Docker Cloud associates the subnet with the Internet Gateway.

### 23.How will you take backup of Docker container volumes in AWS S3?

We can use a utility named Dockup provided by Docker Cloud to take backup of Docker container volumes in S3.

### 24. What are the three main steps of Docker Compose?

Three main steps of Docker Compose are as follows:

Environment: We first define the environment of our application with a Dockerfile. It can be used to recreate the environment at a later point of time.
Services: Then we define the services that make our app in docker-compose.yml. By using this file we can define how these services can be run together in an environment.
Run: The last step is to run the Docker Container. We use docker-compose up to start and run the application.

  
### 25.What is Pluggable Storage Driver architecture in Docker based containers?

Docker storage driver is by default based on a Linux file system. But Docker storage driver also has provision to plug in any other storage driver that can be used for our environment.

In Pluggable Storage Driver architecture, we can use multiple kinds of file systems in our Docker Container. In Docker info command we can see the Storage Driver that is set on a Docker daemon.

We can even plug in shared storage systems with the Pluggable Storage Driver architecture.

###  26. What is Docker Hub?

Docker Hub is a cloud-based registry. We can use Docker Hub to link code repositories. We can even build images and store them in Docker Hub. It also provides links to Docker Cloud to deploy the images to our hosts.

Docker Hub is a central repository for container image discovery, distribution, change management, workflow automation and team collaboration.

### 27.What are the main features of Docker Hub?

Docker Hub provides following main features:

Image Repositories: In Docker Hub we can push, pull, find and manage Docker Images. It is a big library that has images from community, official as well as private sources.
Automated Builds: We can use Docker Hub to create new images by making changes to source code repository of the image.
Webhooks: With Webhooks in Docker Hub we can trigger actions that can create and build new images by pushing a change to repository.
Github/Bitbucket integration: Docker Hub also provides integration with Github and Bitbucket systems.

  
### 28. What are the main security concerns with Docker based containers?

Docker based containers have following security concerns:

Kernel Sharing: In a container-based system, multiple containers share same Kernel. If one container causes Kernel to go down, it will take down all the containers. In a virtual machine environment we do not have this issue.
Container Leakage: If a malicious user gains access to one container, it can try to access the other containers on the same host. If a container has security vulnerabilities it can allow the user to access other containers on same host machine.
Denial of Service: If one container occupies the resources of a Kernel then other containers will starve for resources. It can create a Denial of Service attack like situation.
Tampered Images: Sometimes a container image can be tampered. This can lead to further security concerns. An attacker can try to run a tampered image to exploit the vulnerabilities in host machines and other containers.
Secret Sharing: Generally one container can access other services. To access a service it requires a Key or Secret. A malicious user can gain access to this secret. Since multiple containers share the secret, it may lead to further security concerns.

  
### 29. What are the security benefits of using Container based system?

Some of the main security benefits of using a Container based system are as follows:

Segregation: In a Container based system we segregate the applications on different containers. Each application may be running on same host but in a separate container. Each application has access to ports, files and other resources that are provided to it by the container.
Transient: In a Container based system, each application is considered as a transient system. It is better than a static system that has fixed environment which can be exposed overtime.
Control: We use repeatable scripts to create the containers. This provides us tight control over the software application that we want to deploy and run. It also reduces the risk of unwanted changes in setup that can cause security loopholes.
Security Patch: In a Container based system, we can deploy security patches on multiple containers in a uniform way. Also it is easier to patch a Container with an application update.

  
### 30.How can we check the status of a Container in Docker?

We can use docker ps –a command to get the list of all the containers in Docker. This command also returns the status of these containers.

### 31. What are the main benefits of using Docker?

Docker is a very powerful tool. Some of the main benefits of using Docker are as follows:

Utilize Developer Skills: With Docker we maximize the use of Developer skills. With Docker there is less need of build or release engineers. Same Developer can create software and wrap it in one single file.
Standard Application Image: Docker based system allows us to bundle the application software and Operating system files in a single Application Image that can be deployed independently.
Uniform deployment: With Docker we can create one package of our software and deploy it on different platforms seamlessly.

### 32.How does Docker simplify Software Development process?

Prior to Docker, Developers would develop software and pass it to QA for testing and then it is sent to Build & Release team for deployment.

In Docker workflow, Developer builds an Image after developing and testing the software. This Image is shipped to Registry. From Registry it is available for deployment to any system. The development process is simpler since steps for QA and Deployment etc take place before the Image is built. So Developer gets the feedback early.

### 33.What is the basic architecture behind Docker?

Docker is built on client server model. Docker server is used to run the images. We use Docker client to communicate with Docker server.

Clients tell Docker server via commands what to do.

Additionally there is a Registry that stores Docker Images. Docker Server can directly contact Registry to download images.

### 34.What are the popular tasks that you can do with Docker Command line tool?

Docker Command Line (DCL) tool is implemented in Go language. It can compile and run on most of the common operating systems. Some of the tasks that we can do with Docker Command Line tool are as follows:

We can download images from Registry with DCL.
We can start, stop or terminate a container on a Docker server by DCL.
We can retrieve Docker Logs via DCL.
We can build a Container Image with DCL.
35.    What type of applications- Stateless or Stateful are more suitable for Docker Container?

It is preferable to create Stateless application for Docker Container. We can create a container out of our application and take out the configurable state parameters from application. Now we can run same container in Production as well as QA environments with different parameters. This helps in reusing the same Image in different scenarios. Also a stateless application is much easier to scale with Docker Containers than a stateful application.

### 36.How can Docker run on different Linux distributions?

Docker directly works with Linux kernel level libraries. In every Linux distribution, the Kernel is same. Docker containers share same kernel as the host kernel.

Since all the distributions share the same Kernel, the container can run on any of these distributions.

### 37.Why do we use Docker on top of a virtual machine?

Generally we use Docker on top of a virtual machine to ensure isolation of the application. On a virtual machine we can get the advantage of security provided by hypervisor. We can implement different security levels on a virtual machine. And Docker can make use of this to run the application at different security levels.

### 38.How can Docker container share resources?

We can run multiple Docker containers on same host. These containers can share Kernel resources. Each container runs on its own Operating System and it has its own user-space and libraries.

So in a way Docker container does not share resources within its own namespace. But the resources that are not in isolated namespace are shared between containers. These are the Kernel resources of host machine that have just one copy.

So in the back-end there is same set of resources that Docker Containers share.

### 39.What is the difference between Add and Copy command in a Dockerfile?

Both Add and Copy commands of Dockerfile can copy new files from a source location to a destination in Container’s file path.

They behave almost same.

The main difference between these two is that Add command can also read the files from a URL.

As per Docker documentation, Copy command is preferable. Since Copy only supports copying local files to a Container, it is preferred over Add command.

### 40. What is Docker Entrypoint?

We use Docker Entrypoint to set the starting point for a command in a Docker Image.

We can use the entrypoint as a command for running an Image in the container.

E.g. We can define following entrypoint in docker file and run it as following command:

ENTRYPOINT [“mycmd”]

% docker run mycmd

### 41. What is ONBUILD command in Docker?

We use ONBUILD command in Docker to run the instructions that have to execute after the completion of current Dockerfile build.

It is used to build a hierarchy of images that have to be build after the parent image is built.

A Docker build will execute first ONBUILD command and then it will execute any other command in Child Dockerfile.

### 42. What is Build cache in Docker?

When we build an Image, Docker will process each line in Dockerfile. It will execute the commands on each line in the order that is mentioned in the file.

But at each line, before running any command, Docker will check if there is already an existing image in its cache that can be reused rather than creating a new image.

This method of using cache in Docker is called Build cache in Docker.

We can also specify the option –no-cache=true to let Docker know that we do not want to use cache for Images. With this option, Docker will create all new images.

### 43.What are the most common instructions in Dockerfile?

Some of the common instructions in Dockerfile are as follows:

FROM: We use FROM to set the base image for subsequent instructions. In every valid Dockerfile, FROM is the first instruction.
LABEL: We use LABEL to organize our images as per project, module, licensing etc. We can also use LABEL to help in automation. In LABEL we specify a key value pair that can be later used for programmatically handling the Dockerfile.
RUN: We use RUN command to execute any instructions in a new layer on top of the current image.  With each RUN command we add something on top of the image and use it in subsequent steps in Dockerfile.
CMD: We use CMD command to provide default values of an executing container. In a Dockerfile, if we include multiple CMD commands, then only the last instruction is used.

### 44.What is the purpose of EXPOSE command in Dockerfile?

We use EXPOSE command to inform Docker that Container will listen on a specific network port during runtime.

But these ports on Container may not be accessible to the host. We can use –p to publish a range of ports from Container.

### 45.What are the different kinds of namespaces available in a Container?

In a Container we have an isolated environment with namespace for each resource that a kernel provides. There are mainly six types of namespaces in a Container.

UTS Namespace: UTS stands for Unix Timesharing System. In UTS namespace every container gets its own hostname and domain name.
Mount Namespace: This namespace provides its own file system within a container. With this namespace we get root like / in the file system on which rest of the file structure is based.
PID Namespace: This namespace contains all the processes that run within a Container. We can run ps command to see the processes that are running within a Docker container.
IPC Namespace: IPC stands for Inter Process Communication. This namespace covers shared memory, semaphores, named pipes etc resources that are shared by processes. The items in this namespace do not cross the container boundary.
User Namespace: This namespace contains the users and groups that are defined within a container.
Network Namespace: With this namespace, container provides its own network resources like- ports, devices etc. With this namespace, Docker creates an independent network stack within each container.

### 46.How will you monitor Docker in production?

Docker provides tools like docker stats and docker events to monitor Docker in production.

We can get reports on important statistics with these commands.

Docker stats: When we call docker stats with a container id, we get the CPU, memory usage etc of a container. It is similar to top command in Linux.

Docker events: Docker events are a command to see the stream of activities that are going on in Docker daemon.

Some of the common Docker events are: attach, commit, die, detach, rename, destroy etc.

We can also use various options to limit or filter the events that we are interested in.

### 47.What are the Cloud platforms that support Docker?

Some of the popular cloud platforms that support Docker are:

Amazon AWS
Google Cloud Platform
Microsoft Azure
IBM Bluemix

  
### 48.How can we control the startup order of services in Docker compose?

In Docker compose we can use the depends_on option to control the startup order of services.

With compose, the services will start in the dependency order. Dependencies can be defined in the options like- depends_on, links, volumes_from, network_mode etc.

But Docker does not wait for until a container is ready.

### 49.Why Docker compose does not wait for a container to be ready before moving on to start next service in dependency order?

The problem with waiting for a container to be ready is that in a Distributed system, some services or hosts may become unavailable sometimes. Similarly during startup also some services may also be down.

Therefore, we have to build resiliency in our application. So that even if some services are down we can continue our work or wait for the service to become available again.

We can use wait-for-it or dockerize tools for building this kind of resiliency.

### 50.How will you customize Docker compose file for different environments?

In Docker compose there are two files docker-compose.yml and docker-compose.override.yml. We specify our base configuration in docker-compose.yml file. For any environment specific customization we use docker-compose.override.yml file.

We can specify a service in both the files. Docker compose will merge these files based on following rules:

For single value options, new value replaces the old value.

For multi-value options, compose will concatenate the both set of values.

We can also use extends field to extend a service configuration to multiple environments. With extends, child services can use the common configuration defined by parent service.
