### Occurance
docker container ls is empty when there is a container on docker desktop
### Issue
docker desktop is a different context from the default context in CLI
`` docker context ls
### Solution
change ``docker context use docker-desktop
