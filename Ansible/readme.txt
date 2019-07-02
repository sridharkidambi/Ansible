install Ansible
pip install --user ansible


vagrant:
1.download vagrant
2.install the os from vagrantcloud.com command vagrant box add hashicorp/precise64
3.Initialize it vagrant init hashicorp/precise64
4.Vagrant up (starts vagrant)
5.vagrant ssh

patterns are used for  subset selections

ansible --list-hosts all   list all the hosts.
ansible -m ping webserver ping the servers.
ansible -m command  -a "hostname" all -> runs a command

become used for super user access enablement.
Genia is a templating language library {{item}} used in python.  with_items
