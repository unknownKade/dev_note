: Docker is an open source container management service that stores enviornments in containers to be run on platforms without the hassle of tweaking for each different environment.

### Architecture
- Container Layer
	- read/write layer of containers that sit on top of image layers.
	- handles execution and changes during runtime
	- containers cannot communciate/share with each other
	- communicates to docker engine via ports
- Docker Engine
	- Runs on top of P

### Command
: docker {target} {command} {option} {variable}
- main targets : container, image, volume, network
- main commands : start, stop, create, run, rm, exec, ls, cp, commit, pul, rm, ls, cp, commit, pul, build


`` docker run --name test1 -d httpd