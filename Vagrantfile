Vagrant.configure("2") do |config|

    # Use CentOS 7 as base box
    config.vm.box = "centos/7"

    # Disable VirtualBox Guest additions auto-update
    config.vbguest.auto_update = false

    # Configure VM to use 2 CPU cores and 1 GB of memory
    config.vm.provider "virtualbox" do |vb|
        vb.cpus = "2"
        vb.memory = "1024"
    end

    # Provision machine with Ansible
    config.vm.provision :ansible do |ansible|
        ansible.compatibility_mode = "2.0"
        ansible.playbook = "playbook.yml"
    end

end
