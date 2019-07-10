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

lineinfile:insert a line in a particular file.
wait_for : to check if the particular port is available for connection ;it validates it 
wait_for: port=80 state=drained
register: will save teh executed steps results
template: for file ro render with substitution. ( different to file copy)
 jinja2 template {{value }} to print the values. For loop is in '{%', ends with 'endfor' and the variable is rendered with '{{'
 Roles:
 code reuse logical grouping baased on the components
 ansible-galaxy init control

 Include 
 includes multiple yml files for one set execution
 ansible -m setup sk.com  :to display all  the gathering facts of a instance.

variable precedence  list:

<img width="871" alt="Screenshot 2019-07-09 at 10 48 13 PM" src="https://user-images.githubusercontent.com/8262606/60943307-2efbe400-a303-11e9-8be9-cf884e5d1e11.png">
