# Ansible-Playground
Repo for my default Ansible &amp; Vagrant configurations for a Ansible playground.  

Designed for use on Apple ARM Architecture with [VMware Fusion Public Tech Preview
](https://customerconnect.vmware.com/downloads/get-download?downloadGroup=FUS-PUBTP-2021H1)

Setup ARM Mac with [this gist](https://gist.github.com/sbailliez/f22db6434ac84eccb6d3c8833c85ad92)

### Possible Issues
If networking fails to properly configure, it may require this VMX setting. It can be manually applied via the Vagrantfile:
```
Vagrant.configure(2) do |config|
  config.vm.provider :vmware_desktop do |vmware|
    vmware.vmx["ethernet0.pcislotnumber"] = "160"
  end
end
```