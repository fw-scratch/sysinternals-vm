# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu2204"
  config.vm.provision "shell", inline: <<-SHELL
    wget https://packages.microsoft.com/config/ubuntu/22.04/packages-microsoft-prod.deb
    apt install -y ./packages-microsoft-prod.deb
    apt-get update
    apt-get -y install procdump sysmonforlinux sysinternalsebpf
  SHELL
end
