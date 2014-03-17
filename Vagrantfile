# -*- mode: ruby -*-
# vi: set ft=ruby :

# http://opscode-vm-bento.s3.amazonaws.com/vagrant/virtualbox/opscode_ubuntu-13.10_chef-provisionerless.box

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "chef/ubuntu-13.10"
  config.vm.network :private_network, ip: "192.168.58.58"
  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "jenkins-playbook.yml"
    ansible.host_key_checking = "false"
    ansible.sudo_user = "root"
    ansible.sudo = "true"
  end
end
