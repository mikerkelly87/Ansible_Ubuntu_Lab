Running `ansible-playbook main.yml` in the directory containing these files will 
install lxc and create 16 lxc conatiners. The container named `deploy` will be 
able to ping `server01`-`server15` through ansible with `ansible all -m ping` once 
this playbook has finished.

Before running you will need to edit the `netmask`, `gateway`, and `dns-nameservers`
in the `interfaces.j2` network template file.

You will then need to edit the IP addresses "`ipaddr`" in the `setup_network.yml` 
file.

These edits will need to reflect valid IPs that are in the range of your `lxcbr0` 
network.
