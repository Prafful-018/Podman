# Podman(Docker Alternative)
•	What is Container?

The term and concept ‘container’ came from the shipping container.

i.	These containers are shipped from city to city and country to country.

ii.	No matter which part of the world you go to, you will find these containers with exact same measurements.

iii.	Because around the world all docks, ships and warehouses are built to easily transport and store them.

•	In IT containers are fulfilling similar purpose

Many times, when developer build the code or application, application will run fine on his laptop/PC but when the same application is run by software tester the application will not run in their environment.

i.	Then came the container technology which allowed developers or programmer to test and build applications on any computer just by putting it in a container and then run on another computer regardless of its architecture.

ii.	We can move the application anywhere without moving its OS just like moving the actual physical container anywhere that would fit on any dockyard, truck, ship or warehouse.

iii.	An OS can run single or multiple containers at same time.

•	What is Container Software?

i.	Dockers:  is software used to create and manage containers.

ii.	Podman:  is an alternative to docker. Docker is not supported in RHEL8.It is demon less, open source, designed to develop, manage and run containers.

•	Terms associated with containers.

i.	Images: Containers can be created through images and containers can be converted to images.

ii.	Pods: Group of containers deployed together on the host.

	Building, Running and Managing Containers:

•	Steps for installation

	yum/dnf install podman -y

•	Creating Alias

	alias docker=podman

•	Checking Podman version

	podman -v

•	Checking Podman Registery

	podman info

•	To Search for a image in registry

	podman search nginx

•	Checking already downloaded images

	podman images

•	To download an image

	podman pull docker.io/library/nginx

•	To run an image

	podman run docker.io/library/nginx

•	To see the running containers

	podman ps

•	Port Binding of container

	podman run -dt -p 8080:80/tcp docker.io/library/nginx

•	To stop a container

	podman stop <container_name>

•	To run multiple containers with different port

	podman run -dt -p 8081:80/tcp docker.io/library/nginx

	podman run -dt -p 8082:80/tcp docker.io/library/nginx

•	To name your container will running it

podman run -d --name nginx-container1 docker.io/library/nginx

•	To see all the existing containers

	podman ps -a

•	To remove the existing containers

	podman rm <container_name>
