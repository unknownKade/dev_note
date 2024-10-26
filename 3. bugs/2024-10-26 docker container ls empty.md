### Occurance
docker container ls is empty when there is a container on docker desktop
### Issue
docker desktop is a different context from the default context in CLI
`` docker context ls
### Solution
- change context ``docker context use desktop-linux
- create context ``docker context create desktop-linux --description "Docker Desktop" --docker "host=unix://home/