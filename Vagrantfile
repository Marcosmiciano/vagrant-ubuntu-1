Vagrant.configure("2") do |config|

config.vm.provider "virtualbox" do |v|
  v.name = "VAGRANT-UBUNTU"
  v.memory = "1024"
  v.cpus = "1"
end

  config.vm.box = "hashicorp/bionic64"  
  config.vm.network "forwarded_port", guest: 80, host: 8091
  config.vm.network "public_network", ip: "192.168.10.100", bridge:"Intel(R) Wireless-AC 9560"
  config.vm.provision "shell", path: "script.sh"
  config.vm.synced_folder "vagrant-shell-script-nginx/" , "/var/www/html"
end
