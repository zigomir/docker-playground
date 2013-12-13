# Learning docker

```bash
vagrant up
vagrant ssh
cd /vagrant
docker build . # build container from Dockerfile
```

## tagging

```bash
docker images # list images
docker tag 9384910aefa3 ruby:latest # tag last image if needed
```

## test it

```bash
docker run ruby:latest ruby -v # run command on image (inside the container)
```

## interactive mode

```bash
docker run -i -t ruby:latest irb
```


## commit and push image

```bash
docker ps -l # list containers
docker commit b42ffbb8d864 zigomir/ruby
docker login # log in to your docker index profile
docker push zigomir/ruby
```

Now we got many images because of Dockerfile's `RUN` commands which commits stuff.
[Here](https://github.com/dotcloud/docker/issues/332) is the debate about flattening your
images, but I guess this feature isn't supported yet.
