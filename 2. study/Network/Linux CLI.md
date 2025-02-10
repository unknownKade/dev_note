
```shell
clear
cd # cd - goes back to first dir
ls [flags] [directory]
	-l #include permissions,size,timestamps
	-a -all #include hidden files

pwd #current path
mkdir #new dir
	-p ./home/{a,b}/{x,y,z} #makes a,b folders with x,y,z inside
touch #new file
	file{1..10}.txt #makes 10 text files
rm #delete
cp #copy
mv [file] [to] #move
ln [target] [link name] #hard link
	-s #symbolic link
tail [flag] [file] #see end of file
	-f #follow changes
 history #history of past commands
```

```shell

lsb_release -a #shows os version
#update ubuntu
sudo apt update
sudo apt-get update
#install java
sudo apt-cache search jdk
sudo apt-cache search jdk | grep openjdk-11
sudo apt install openjdk-11-jdk

```


### Process
```shell
ps 
	-e #all processes for all users
	-f #full format details
	-l #long format details
kill [flag] [PID]
	-KILL
	-9
	-l

```

### Network

```shell
netstat -nlpt #monitor active internet connections

```

## Vim
```shell
mkdir nodejsapp
vi app.js #write text :wq on to exit


```

### References
[difference between apt apt-get](https://aws.amazon.com/ko/compare/the-difference-between-apt-and-apt-get/)
