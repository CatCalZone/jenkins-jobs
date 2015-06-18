Vagrant.configure(2) do |config|

  config.vm.box = "chef/ubuntu-14.04"
  config.omnibus.chef_version = "12.3.0"

  config.vm.define :jenkins do |jenkins|
    jenkins.vm.network :forwarded_port, guest: 8080, host: 8080

    jenkins.toplevel_cookbook.url = "https://github.com/Zuehlke/cookbooks-jenkins-simple-app"
    jenkins.vm.provision :chef_solo do |chef|
      chef.add_recipe "jenkins-simple-app::default"
    end
  end

end
