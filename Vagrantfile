# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.provision "shell", inline: <<-SHELL
    sed -i 's/ChallengeResponseAuthentication no/ChallengeResponseAuthentication yes/g' /etc/ssh/sshd_config   
    sudo systemctl restart sshd  
  SHELL
  config.vm.provision "ansible" do |ansible|
    ansible.config_file = "ansible.cfg"
    ansible.inventory_path = "inventory"
    ansible.playbook = "playbook.yml"
    ansible.limit = "gitea_hosts"
  end
end
