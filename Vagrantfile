Vagrant.configure("2") do |config|

  # Running standard Ubuntu 64 bits version
  config.vm.box = "ubuntu/trusty64"

  config.vm.network "forwarded_port", guest: 3000, host: 3000 		  # Node.js
  config.vm.network "forwarded_port", guest: 27017, host: 27017   	# MongoDB

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  config.vm.network "private_network", ip: "192.168.33.10"

  # Set up a synced folder
  config.vm.synced_folder "/Users/franverona/Documents/vagrant", "/vagrant_data"

  # Provision VM only once
  config.vm.provision :shell, :path => "provision.sh"

end
