Vagrant.configure("2") do |config|
  # Configuración de máquina Venus (Debian texto)
   config.vm.box = "debian/bookworm64"
   config.vm.network "forwarded_port", guest: 80, host: 80 
   config.vm.provision "shell", inline: <<-SHELL
     apt-get update
     apt-get install -y apache2
     cp -v /vagrant/apache2.conf /etc/apache2
   SHELL
 end