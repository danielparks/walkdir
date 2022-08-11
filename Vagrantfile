# -*- mode: ruby -*-
# vi: set ft=ruby :

# FIXME delete this file before submitting PR
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/jammy64"
  config.vm.provision "shell", inline: <<-SHELL
    export DEBIAN_FRONTEND=noninteractive
    apt-get update
    apt-get dist-upgrade
    apt-get install -y build-essential curl
    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs \
      | sudo -u vagrant -i sh -s -- -y
  SHELL
end
