# APP documentation
- Contains provisioning file to update and install nginx
- Allows for nginx to launch just by entering vagrant up
## Provision.sh file
```
#!/bin/bash
# update system
sudo apt-get update -y
# upgrade system
sudo apt-get upgrade -y
# install nginx
sudo apt-get install nginx -y

# load nginx on 192.168.10.100
```
- Added ```config.vm.provision :shell, path: "app/provision.sh"``` to vagrant file which allows for the vagrant up to launch bash script
- Found here: https://www.vagrantup.com/docs/provisioning/shell