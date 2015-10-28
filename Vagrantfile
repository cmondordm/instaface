Vagrant.configure(2) do |config|

     config.vm.define "instaface" do |box|

       box.vm.box = "puppetlabs/centos-7.0-64-puppet"
       box.vm.host_name = "instaface.dev.local"
       box.vm.network "private_network", ip: "192.168.50.50"

#       box.vm.provision "shell", 
#       inline:  "yum clean all"

#       box.vm.provision :puppet do |puppet|
#        puppet.module_path = ['modules']
#        puppet.manifest_file = 'site.pp'
#      end
    end
end
