Vagrant.configure("2") do |config|
    # General configuration
    config.vm.box = "generic/ubuntu2004"
    config.ssh.insert_key = false

    config.vm.provider :virtualbox do |v|
        v.memory = 512
        v.linked_clone = true
    end

    # VM configuration
    config.vm.define "ubuntu2004" do |ubuntu2004|
        ubuntu2004.vm.hostname = "ansible"
    end

    config.vm.provision "ansible" do |ansible|
        ansible.playbook = "playbook.yml"
    end
end
