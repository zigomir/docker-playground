# Learning docker

```bash
vagrant up
vagrant ssh
cd /vagrant
docker build . # to run Dockerfilee
```

## tagging

```bash
docker tag 9384910aefa3 ruby:latest
```

## test it

```bash
docker run ruby:latest ruby -v
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
