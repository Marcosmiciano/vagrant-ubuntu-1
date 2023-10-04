Vagrant.configure("2") do |config|

config.vm.provider "virtualbox" do |v|
  v.name = "PRIMEIRA-MAQUINA-VAGRANT-01"
  v.memory = "2048"
  v.cpus = "3"
end

  config.vm.box = "hashicorp/bionic64"  
  config.vm.network "forwarded_port", guest: 80, host: 8090
  config.vm.network "public_network", ip: "192.168.10.100", bridge:"Intel(R) Wireless-AC 9560"
  config.vm.provision "shell", path: "script.sh"
  config.vm.synced_folder "site/" , "/var/www/html"
end
