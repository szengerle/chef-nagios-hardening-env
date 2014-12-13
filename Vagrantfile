Vagrant.configure("2") do |config|

  config.vm.network "forwarded_port", guest: 80, host: 10080
  
  config.vm.define "nagios-hardening" do |c|
    c.vm.box = "trusty32"
    c.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-i386-vagrant-disk1.box"

    c.vm.provision :shell, inline: "apt-get update"
    
    c.vm.provision :chef_solo do |chef|
      chef.cookbooks_path = ["cookbooks", "site-cookbooks"]
      chef.roles_path = "roles"
      chef.data_bags_path = "data_bags"
      chef.add_role "nagios-hardening"
    end
    
  end

end
