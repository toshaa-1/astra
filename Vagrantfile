ENV['VAGRANT_DEFAULT_PROVIDER'] = 'virtualbox' 


Vagrant.configure("2") do |config|
  config.vm.box = "astra"
  

# server 1
  config.vm.define "node1" do |node1|
	  node1.vm.hostname = "astra1.local"
	  node1.vm.network "forwarded_port", guest: 22, host: 2223
	  node1.vm.network "forwarded_port", guest: 80, host: 8080
	  node1.vm.provider "virtualbox" do |vb|
		vb.gui = true
		vb.memory = "4048"
		vb.cpus = "3"
      end
  end



# server 2
  config.vm.define "node2" do |node2|
	  node2.vm.hostname = "astra2.local"
	  node2.vm.network "forwarded_port", guest: 22, host: 2224
	  node2.vm.network "forwarded_port", guest: 80, host: 8081
	  node2.vm.provider "virtualbox" do |vb|
		vb.gui = true
		vb.memory = "3036"
		vb.cpus = "2"
	  end
  end


# server 3
  config.vm.define "node3" do |node3|
	  node3.vm.network "forwarded_port", guest: 22, host: 2225
	  node3.vm.network "forwarded_port", guest: 80, host: 8082
	  node3.vm.provider "virtualbox" do |vb|
		vb.gui = true
		vb.memory = "2024"
		vb.cpus = "2"
	  end
  end
end
