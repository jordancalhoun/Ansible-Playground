# Ansible-Playground

Repo for my default Ansible &amp; Vagrant configurations for a Ansible playground.

## Setup

1. If running a Mac with Apple ARM architecture, first follow [this gist](https://gist.github.com/sbailliez/f22db6434ac84eccb6d3c8833c85ad92)
2. Clone Repo
3. `cd` into repo
4. Run `vagrant up intel` for x86 architecture, `vagrant up arm` for ARM.
5. Create desired plays in `playbook.yml`
6. Run `ansible-playbook -i inventory.yml playbook.yml`

You now have a Ansible ready VM at `192.168.60.10`

---

### Possible Issues

If networking fails to properly configure, it may require this VMX setting. It can be manually applied via the Vagrantfile:

```
Vagrant.configure(2) do |config|
  config.vm.provider :vmware_desktop do |vmware|
    vmware.vmx["ethernet0.pcislotnumber"] = "160"
  end
end
```
