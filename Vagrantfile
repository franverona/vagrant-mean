# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  # Running standard Ubuntu 64 bits version
  config.vm.box = "ubuntu/trusty64"

  # Check for VM updates on every 'vagrant up' (it never updates, just check for them)
  config.vm.box_check_update = false

 # config.vm.network "forwarded_port", guest: 3000, host: 3000 		# Node.js
 # config.vm.network "forwarded_port", guest: 27017, host: 27017   	# MongoDB

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  config.vm.network "private_network", ip: "192.168.33.10"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # config.vm.network "public_network"

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  config.vm.synced_folder "/Users/franverona/Documents/vagrant", "/vagrant_data"

  # Provision VM only once
  config.vm.provision :shell, :path => "provision.sh"

end
