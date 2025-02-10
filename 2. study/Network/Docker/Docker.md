: Docker is an open source container management service that stores enviornments in containers to be run on platforms without the hassle of tweaking for each different environment.

[[Dockerfile]]
[[Docker-Compose]]

### Architecture
- Container Layer
	- R/W layer of containers that sit on top of image layers.
	- handles execution and changes during runtime
	- containers cannot communciate/share with each other
	- communicates to docker engine via ports
	- communicate to other container via port ``-p $host_port : $container_port
- Image Layer
	- R/O shared layer of images underneath container layer
	- images are shared between containeres = enhances performance
- Docker Engine
	- Runs on top of the computer and communicates to containers

### Command
: docker {target} {command} {option} {variable}
- main targets : container, image, volume, network
- main commands 
	- start
	- stop
	- create
	- run
	- rm
	- exec
	- ls 
	- cp
	- commit
	- pull
	- commit
	- build
- make a container named test1 that runs in background `` docker run --name test1 -d httpd
- host port 8080 and set network and container port 80 ``docker run --name test1 -d -p 8080:80 httpd`` -> It works! page in localhost
- show all containers regardless of state``docker ps -a