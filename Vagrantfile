Vagrant.configure("2") do |config|
  # Spécifier la boîte de base (système d'exploitation virtuel)
  config.vm.box = "ubuntu/bionic64"
  
  # Configuration réseau
  config.vm.network "forwarded_port", guest: 80, host: 8080
  
  # Provisionnement (installation d'Apache par exemple)
  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
    sudo apt-get install -y apache2
  SHELL
end