Vagrant.configure("2") do |config|
  config.vm.box     = 'docker-ready-precise64'
  config.vm.box_url = 'http://nitron-vagrant.s3-website-us-east-1.amazonaws.com/vagrant_ubuntu_12.04.3_amd64_virtualbox.box'

  config.vm.provision :shell, :inline => 'apt-get update --fix-missing'
  config.vm.provision 'docker' do |d|
    d.pull_images 'ubuntu'
    # d.run "rabbitmq"
  end
end
