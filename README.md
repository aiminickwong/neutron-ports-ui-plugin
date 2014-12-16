# Introduction
A UI plugin of oVirt webadmin to show ports details of networks imported from external neutron network provider.

# Installation and Setup
1. Copy the following files from the repository and place them in /usr/share/ovirt-engine/ui-plugins on the host running oVirt Engine:
  * neutron-ports.json
  * neutron-ports-resources/plugin.html
  * neutron-ports-resources/neutron-ports.html
2. Copy the following file and place it in /etc/httpd/conf.d/ on the oVirt Engine server to setup Apache mod_proxy:
  * ovirt-engine-neutron-ports-plugin.conf
3. Change hostnames and ports in the configuration files according to your environment

# Known Issues
* ONLY one neutron server can be configured
* The name of the imported network SHOULD be the same as it is in neutron, due to no available REST API could be used to get the external id infomation of an imported network

# TODO
* Show information of VMs/NICs to which the ports are attached
* Ports management?(adding, editing, deleting, ...)
* UI/UX improvement
