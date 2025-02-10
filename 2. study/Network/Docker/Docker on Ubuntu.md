

```shell
# docker engine gpg 키 등록
sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

# apt source 에 docker 관련 추가
echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update

# docker engine 설치
sudo apt-get install -y docker-ce docker-ce-cli containerd.io \
docker-buildx-plugin docker-compose-plugin docker-compose

#give user docker authority
sudo usermod -aG docker {user}
sudo groupadd docker
sudo service docker restart #restart to implement
sudo systemctl status docker #check service status

#docker login
docker login
docker login -u {krillContainer}
docker logout

# images
docker images
docker image pull nginx:1.25.3-alpine
docker pull gcr.io/googlesamples/hello-app:1.0 #sample of pulling a private repo
docker image inspect --format="{{.RepoTags}}" ngnix #inspect image
docker image history nginx:latest

docker run -d -p 8001:80 --name webserver01 nginx:1.25.3-alpine
docker ps | grep webserver01 #list containers
docker port webserver01
curl localhost:8001

#container
docker create -ti --name ubuntutest ubuntu #create ubuntu container
docker ps -a #show contianers

docker start ubuntutest
docker attach ubuntutest
docker run -ti --name=ubuntutest2 ubuntu /bin/bash
docker buildx build -t node-test:1.0
```