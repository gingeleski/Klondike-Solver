# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = 4096
    vb.cpus = 2
    vb.name = "vm-cpp"
  end

  config.vm.provision "shell", inline: <<-SHELL
    yum update -y
    yum install -y epel-release
    yum install -y gcc-c++ cmake3 make rpm-build valgrind pam-devel ncurses-devel openssl-devel
    yum install -y git
  SHELL
end
