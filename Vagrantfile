Vagrant.configure("2") do |config|
 
  # configure the VM settings
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip:"192.168.10.100"

  # provision the VM to have nginx web server
  config.vm.provision "shell", path: "provision.sh"

  # move app folder from local machine to the VM
  # ("/" at start of filepath to indicate user not root)
  config.vm.synced_folder "app", "/home/vagrant/app"

end
