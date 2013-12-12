vagrant up
vagrant ssh
cd /vagrant
docker build . # to run Dockerfilee

# tagging
docker tag 9384910aefa3 ruby:latest

# test it
docker run ruby:latest ruby -v

# interactive mode
docker run -i -t ruby:latest irb


# commit and push image
docker ps -l

docker commit b42ffbb8d864 zigomir/ruby
docker login # log in to your docker index profile
docker push zigomir/ruby
