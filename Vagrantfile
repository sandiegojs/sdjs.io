# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.box = "ubuntu/trusty64"
    config.vm.synced_folder './', '/vagrant/', id: 'vagrant-root', nfs: true
    config.vm.provision :shell, path: 'provision.sh'

    config.vm.provider "virtualbox" do |v|
        v.name = "sdjs.io.dev"
        v.memory = 2048
    end

    config.vm.hostname = 'sdjs.io.dev'
    config.vm.network :private_network, ip: '172.16.5.124'

end
