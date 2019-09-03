docker version
docker-machine ls
docker-machine start default
docker-machine stop default
docker-machine env default
	eval $("C:\Program Files\Docker Toolbox\docker-machine.exe" env default)
docker-machine active
docker-machine ip default
docker-machine create --driver virtualbox node1

docker container run hello-world
docker container run -it alpine sh
	cat /etc/os-release
	uname -r
	^Ctrl+D: To terminate container and exit -it
	^Ctrl+P then Ctrl+Q: To run container in background and exit -it`
docker container run -it ubuntu sh
docker container ls
docker container attach kind_hawking
docker container ls
docker container start kind_hawking
docker container stop kind_hawking
docker container run -itd alpine sh
docker container ls -a
docker container rm d610b552c56e
docker container ls -aq
docker container rm $(docker container ls -aq)
docker image ls
docker image rm hello-world
docker container run --rm hello-world
docker container ls -a
docker container run --name my_container hello-world
docker container ls -a
docker container run nginx
docker container run -p 80:80 nginx
docker container run -p 8080:80 nginx
docker container run --rm -it --name c1 alpine sh
	ifconfig eth0
docker container run --rm -it --name c2 --link c1 alpine sh
	ping c1
docker network ls
docker network create test
docker container run -it --rm --network test --name c1 alpine sh
docker container run -it --rm --network test --name c2 alpine sh
	ping c1
docker login
docker image build -t myalpine:latest .
docker container run -it myalpine:latest	
docker image tag navaneeths/myalpine:latest navaneeths/myalpine:latest 
docker image push navaneeths/myalpine:latest 
docker container run --name c1 --rm -d nginx:latest
docker container exec c1 cat /etc/nginx/nginx.conf
docker container exec -it c1 sh
docker container run -i alpine
ls -l
docker container run -t alpine
ls -l
docker container run -it alpine
ls -l
docker container run --name c1 nginx:latest
docker container stop c1
# kills pid 1 with SIGTERM - Exited(0)
docker container ls -a
docker container run --name c2 navaneeths/stop_demo:latest
docker container stop c2
docker container run --name c3 navaneeths/stop_demo:latest
docker container kill c3
# kills pid 1 with SIGKILL - Exited(137)
docker container kill --help
# Ctrl+C sends SIGINT
docker image build -t navaneeths/nginx:latest . && docker container run --rm navaneeths/nginx:latest
docker container run --rm --name c1 -p 80:80 nginx:latest
curl localhost
docker container run --rm --name c1 -p 80:80 -d nginx:latest
curl localhost
docker container logs c1
docker container logs -f c1
curl localhost
docker container run --rm --name c1 -p 80:80 navaneeths/nginx:latest
docker container exec c1 tail /var/log/nginx/access.log
docker image build -t navaneeths/nginx:latest .
docker container run --rm --name c1 -p 80:80 navaneeths/nginx:latest
















































