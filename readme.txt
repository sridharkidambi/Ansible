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

<img width="871" alt="Screenshot 2019-07-09 at 10 48 13 PM" src="https://user-images.githubusercontent.com/8262606/60909382-bdd51600-a29b-11e9-923e-f0743004563b.png">
Group_vars:
used to put the global varaibles across playbooks.

Vault for encrypting:
create: ansible-vault create vault
edit: ansible-vault edit vault
ansible-playbook  --ask-vault-pass

Ansible hub: reusable ,sharing ansible content


limit:
limit the hosts while execution --limit server#1

### time taken for execution:
time ansible-playbook playbook/installs.yml --list-tags

### tags associted:
ansible-playbook playbook/installs.yml --list-tags
ansible-playbook playbook/installs.yml --tags "packages"
ansible-playbook playbook/installs.yml --skip-tags "packages"

ignore_errors: true ( to excluede error while executing a task.)

--step ( used to run a particular step from command line.)
--start-at-task ( to start from a particular task.)
ansible-playbook --syntax-check site.yml
ansible-playbook  --check  app.yml ( to check the steps)
-debug: var=someregister variable(for an example).

to retry with the inbbuilt retry logic from ansible use the below
ansible-playbook app.yml --limit @path provided by ansible.
