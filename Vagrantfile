Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu2004"
  config.vm.box_check_update = false
  config.vm.hostname = "focal01"
  config.vm.network "forwarded_port", guest: 3000, host: 3000
  config.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = "2"
  end
  config.vm.provision "ansible" do |ansible|
    ansible.become = true
    ansible.verbose = "v"
    ansible.playbook = "playbook.yml"
    ansible.compatibility_mode = "2.0"
end
     end
