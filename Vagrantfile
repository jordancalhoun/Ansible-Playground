Vagrant.configure(2) do |config|
  
  config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant", disabled: true
  
  #Create the ARM based vm.
  config.vm.define "arm" do |app|
    config.vm.box = "spox/ubuntu-arm"
    app.vm.hostname = "ansible-playground"
    app.vm.network :private_network, ip: "192.168.60.10"
  end
  
  #Create the intel based vm. 
  config.vm.define "intel" do |app|
    config.vm.box = "ubuntu/focal64"
    app.vm.hostname = "ansible-playground"
    app.vm.network :private_network, ip: "192.168.60.10"
  end
end