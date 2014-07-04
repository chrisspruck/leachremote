# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "genebean/centos6-64bit"

  config.vm.hostname = "leachremote"

  config.vm.provision "shell", path: "scripts/puppet.sh"

  config.vm.provision "puppet" do |puppet|
    puppet.module_path = "modules"
  end

  config.vm.provider "vmware_fusion" do |v|
    v.gui = false
  end

  config.vm.provider "virtaulbox" do |v|
    v.gui = false
  end

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # config.vm.network "forwarded_port", guest: 80, host: 8080

end
