Vagrant.configure("2") do |config|
  # Define la imagen base que se usara para configurar la maquina virtual
  # En este caso es una imagen de ubuntu modificada para Vagrant
  config.vm.box = "hashicorp/bionic64"

  # Permite redireccionar un puerto del host a la maquina virtual
  config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

  # Al provisionar la maquina ejecuta este script lo que permite instalar apps
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y apache2
  SHELL
end
