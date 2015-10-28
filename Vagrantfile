Vagrant.configure(2) do |config|

     config.vm.define "instaface" do |box|

       box.ssh.forward_agent = true

       box.vm.box = "puppetlabs/centos-7.0-64-puppet"
       box.vm.host_name = "instaface.dev.local"
       box.vm.network "private_network", ip: "192.168.50.50"

#       box.vm.provision "shell", 
#       inline:  "yum clean all"

#       box.vm.provision :puppet do |puppet|
#        puppet.module_path = ['modules']
#        puppet.manifest_file = 'site.pp'
#      end

    box.vm.synced_folder "~/.composer", "/home/vagrant/.composer",
        owner: "vagrant", group: "vagrant",
        mount_options: ["dmode=777","fmode=777"]

    box.vm.synced_folder ".", "/app",
        owner: "vagrant", group: "vagrant",
        mount_options: ["dmode=777","fmode=777"]

    config.vm.provider "virtualbox" do |v|
      v.customize ["modifyvm", :id, "--memory", "4096"]
      v.customize ["modifyvm", :id, "--cpus", "2"]
    end

    end
end
