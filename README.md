# A Cloud9 docker image based on Ubuntu 22.04 (Jammy)

## Base Docker Image
[Ubuntu](https://hub.docker.com/_/ubuntu) 22.04 (x64)

## Get the image from Docker Hub or build it locally
```
docker pull fullaxx/cloud9-jammy
docker build -t="fullaxx/cloud9-jammy" github.com/Fullaxx/cloud9-jammy
```

## Run the image on port 80
```
docker run -d -p 80:80 fullaxx/cloud9-jammy
```

## Save your Cloud9 workspace on the host
```
docker run -d -p 80:80 -v /srv/docker/c9ws/:/c9ws/ fullaxx/cloud9-jammy
```

## Use Basic Auth when connecting
```
docker run -d -p 80:80 \
-e C9USER=user -e C9PASS=pass \
-v /srv/docker/c9ws/:/c9ws/ \
fullaxx/cloud9-jammy
```
