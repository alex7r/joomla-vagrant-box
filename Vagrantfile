Vagrant.configure("2") do |config|
  config.vm.box = "thealex7r/joomla"
  config.vm.network "private_network", ip: "192.168.33.10"
  # config.vm.network "public_network"
  config.vm.synced_folder ".", "/vagrant", :mount_options => ["dmode=777", "fmode=777"]
  config.vm.provision "shell", inline: <<-SHELL
    mv /var/www/html /vagrant/html
    rm -f /var/www/html
    ln -s /vagrant/html /var/www/html
  SHELL
end