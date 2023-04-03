# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|

  config.vm.box = "bento/ubuntu-20.04"
  config.vm.network "public_network"
  # config.vm.network "public_network"


  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "init-playbook.yml"
  end

  config.vm.define :vm1 do |vm1|
    vm1.vm.hostname = "vm1" 
    vm1.vm.provision :shell, inline: "echo vm1"
  end

  config.vm.define :vm2 do |vm2|
    vm2.vm.hostname = "vm2" 
    vm2.vm.provision :shell, inline: "echo vm2"
  end

  config.vm.define :vm3 do |vm3|
    vm3.vm.hostname = "vm3" 
    vm3.vm.provision :shell, inline: "echo vm3"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "init-playbook.yml"
  end

end