
### EC2

- launch instance
- push to remote repository
- download project to EC2
- project test and build
- run on background with nohup
- log errors
- auto restart server with cron

```shell
chmod u+x gradlew #make project jar
sudo apt update
sudo apt-cache search jdk | grep openjdk-17 #search java17
sudo apt install openjdk-17-jdk #install java17
java --version #check java version
./gradlew build #build gradle
```