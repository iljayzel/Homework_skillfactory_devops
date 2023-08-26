Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"  # Используем образ Ubuntu 18.04
  config.vm.network "private_network", type: "dhcp"  # Приватная сеть
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"  # Выделяем 1 ГБ оперативной памяти
  end

  config.vm.provision "shell", inline: <<-SHELL
    # Обновляем пакеты
    sudo apt-get update

    # Устанавливаем PostgreSQL 8.4
    sudo apt-get install -y postgresql-8.4
  SHELL
end