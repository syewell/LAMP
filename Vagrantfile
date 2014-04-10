# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"
  config.vm.network :private_network, ip: "192.168.25.25"
  config.vm.provision :shell, :inline => "ulimit -n 4048"
  config.vm.provision :shell, :path => "install.sh"
  config.vm.synced_folder ".", "/var/www", :owner=>'vagrant', :group=>'www-data', :mount_operations=> ['dmode=775', 'fmode=775']
end
