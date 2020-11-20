# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "Yi-Tseng/onie"
  config.vm.box_version = "1.0.0"
  config.ssh.username = "root"
  config.ssh.shell = "sh"
  config.vm.synced_folder '.', '/vagrant', disabled: true
  config.vm.provider :virtualbox do |vb|
    vb.memory = 1024
    vb.cpus = 2
    vb.gui = false
    vb.name = "onie"
    vb.customize ["modifyvm", :id, "--uart1", "0x3f8", "4"]
    vb.customize ["modifyvm", :id, "--uartmode1", "tcpclient", "127.0.0.1:8999"]
  end
end

