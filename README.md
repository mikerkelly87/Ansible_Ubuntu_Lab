Running the main.yml playbook will install lxc and create 16 lxc conatiners
The container named deploy will be able to ping server01-server15 through ansible
with `ansible all -m ping` once this playbook has finished.