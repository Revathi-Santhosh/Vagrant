Vagrant.configure("2") do |config|
  config.vm.box = "bento/centos-7.2"
  config.vm.hostname = "ansibletesthost"
  config.vm.network "private_network", ip: "192.168.50.4"
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "site.yml"
    ansible.inventory_path = "inventory.yml"
    ansible.compatibility_mode = "2.0"
    ansible.limit = "all"
  end
  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
    v.cpus = 2
  end
end
