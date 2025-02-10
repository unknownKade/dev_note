
## Occurance
- when to pull nginx docker image in ubuntu given error:
  ``Cannot connect to the Docker daemon at unix:///var/run/docker.sock. Is the docker daemon running?``

## Issue
- checked if docker was running ``sudo systemctl status docker
- give ubuntu authorization 
	``sudo groupadd docker
	``sudo usermod -aG docker user
- restart
	``systemctl start docker
	``systemctl enable docker
	``systemctl daemon-reload
- see dockerd log ``journalctl -fu docker


### Solution
rebooted computer