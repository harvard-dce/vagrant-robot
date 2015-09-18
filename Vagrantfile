# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "robot" do |robot|
    robot.vm.box = "ubuntu/trusty64"
    robot.vm.network "private_network", ip: "192.168.51.10"

    robot.vm.provision "ansible" do |ansible|
        ansible.playbook = 'playbooks/robotframework-box.yml'
    end

    robot.vm.provider 'virtualbox' do |v|
        v.memory = 4096
        v.cpus = 1
    end
  end

end
