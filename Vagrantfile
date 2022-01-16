Vagrant.configure(2) do |config|
  config.vm.box = "spox/ubuntu-arm"
  config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant", disabled: true
  
  
  #Create the vm. 
	config.vm.define "app1" do |app|
	  app.vm.hostname = "orc-app1.test"
	  app.vm.network :private_network, ip: "192.168.60.10"
	end
end