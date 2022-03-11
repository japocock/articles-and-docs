#### Docker

Pull a docker image

```sh
#docker pull #Pull a container 

#docker pull ubuntu #Pull ubuntu

#docker pull ubuntu:latest (Specify tag e.g. latest)

``

View iamges

```sh
#docker images

PS C:\WINDOWS\system32> docker images
REPOSITORY          TAG       IMAGE ID       CREATED        SIZE
ubuntu              latest    fb52e22af1b0   6 days ago     72.8MB

``

Inspect Image

```sh
#docker images

#PS C:\WINDOWS\system32> docker images
#REPOSITORY          TAG       IMAGE ID       CREATED        SIZE
#ubuntu              latest    fb52e22af1b0   6 days ago     72.8MB

``

Inspect Image

```sh

docker inspect fb52e22af1b0

``

Run image

```sh
#docker images

docker run -d -name UBUNTU fb52e22af1b0

``

Run image

```sh

#In the background
docker run -d -name UBUNTU fb52e22af1b0

#Interactive
docker run -it fb52e22af1b0

``
https://www.digitalocean.com/community/tutorials/how-to-remove-docker-images-containers-and-volumes

