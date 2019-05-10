# vi: set ft=ruby :

ENV['VAGRANT_NO_PARALLEL'] = 'yes'

Vagrant.configure(2) do |config|

  config.vm.synced_folder ".", "/vagrant", type: "virtualbox"
  config.vm.synced_folder "../../data", "/data"

  #config.vm.provision "shell", path: "bootstrap.sh"

  config.vm.define "docker1" do |docker1|
    docker1.vm.box = "centos7v3"
    docker1.vm.hostname = "docker1.example.com"
    docker1.vm.network "private_network", ip: "172.42.42.31"
    docker1.vm.provider "virtualbox" do |vb|
      vb.name = "docker1"
      vb.memory = 3064
      vb.cpus = 2
    end
  end

  config.vm.define "docker2" do |docker2|
    docker2.vm.box = "centos7v3"
    docker2.vm.hostname = "docker2.example.com"
    docker2.vm.network "private_network", ip: "172.42.42.32"
    docker2.vm.provider "virtualbox" do |vb|
      vb.name = "docker2"
      vb.memory = 512
      vb.cpus = 1
    end
  end

end
