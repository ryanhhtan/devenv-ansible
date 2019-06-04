Vagrant.configure("2") do |config|
    # The box to be used
    config.vm.box = "ubuntu/xenial64"
    config.vm.synced_folder ".", "/vagrant", :mount_options => ["dmode=755", "fmode=600"]
    config.disksize.size="20GB"
    
    # Set memory for the VM 
    config.vm.provider "virtualbox" do |vb|
        vb.gui = false
        vb.memory = "4096"
    end

    config.vm.define "devserver" do |devserver|
        devserver.vm.hostname = "devserver"
        devserver.vm.network "private_network", ip: "192.168.2.222"
        devserver.vm.synced_folder "d:\\", "/d"
        devserver.vm.provision "ansible_local" do |ansible|
            ansible.playbook = "playbook.yml"
            ansible.inventory_path = "inventory"
            ansible.install = true
        end
    end
end
