Vagrant.configure("2") do |config|
    config.vm.box = "hashicorp/precise64"
    config.vm.provision :shell, path: "setup_host.sh"
    config.vm.provision :shell, path: "setup_joomla.sh"
    config.vm.provision :shell, path: "fix_htaccess.sh"
    config.vm.provision :shell, path: "cleanup.sh"
    config.vm.network "private_network", ip: "192.168.33.111"
end