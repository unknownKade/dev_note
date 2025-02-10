docker build {option} {dockerfile_directory}
example
- docker build -t test
- docker run --name test_app -p 80:80 test

## Commands
- FROM : make image from a certain base(ex. OS image)
- RUN : build image command
- ADD : add file/directory to image from host
- COPY : copy file/directory to image
- EXPOSE : expose image port 
- ENV : set enviornment $name: -else : name
- CMD : set command to be run when container is run
- ENTRYPOINT :
- WORKDIR : set directory for RUN, CMD, ENTRYPOINT. overridde with -w option
- VOLUME : for persistence data
- SHELL
- LABEL
- USER
- ARG
- STOPSIGNAL
- HEALTHCHECK


### Example
```
FROM httpd

COPY index.html /usr/local/apache2/htdocs/
```