Vagrant.configure("2") do |config|

	ENV["LC_ALL"] = "en_US.UTF-8"

	config.vm.box = "centos/7"
	config.vm.hostname = "apacheds.local"

	config.vm.synced_folder ".", "/vagrant", disabled: true

	config.vm.network "forwarded_port", guest: 10389, host: 10389, host_ip: "127.0.0.1"
	config.vm.network "forwarded_port", guest: 10636, host: 10636, host_ip: "127.0.0.1"

	config.vm.provider "virtualbox" do |v|
		v.name = "apacheds"
	end

	config.vm.provision "ansible" do |ansible|
		ansible.verbose = "v"
		ansible.compatibility_mode = "2.0"
		ansible.playbook = "playbook.yml"
	end

end
