# Prepare Ansible controller and prepare managed nodes in automated fashion

## Scenario
Since you have just installed your VM guest machines, they have no software installed on them. We need to prepare their environment using Ansible.

## Tasks
* Add user "ansible" and create directory /home/ansible/automation.
* Add the user to sudoers. The user must be able to login as root without being prompted for root password.
* Install python3.
* Install python module "ansible" for user "ansible".
* Generate SSH RSA key pair which is 2048 bits long.
* Create an inventory file in /home/ansible/automation called "inventory"
* Create the following hosts groups and assing the following hosts to them:
	* group "loadbalancers", hosts: lb.example.com
	* group "web", hosts: web1.example.com, web2.example.com
	* group "database", hosts: db.example.com
* Create a simple BASH script, that uses Ansible ad-hoc commands to do the following:
	* Import your public SSH key to the user Ansible.
	* Install python3 on all remote hosts.
	* Create user "ansible" on all remote hosts (lb.example.com, web1.example.com, web2.example.com and db.example.com).
	* Add the user "ansible" to sudoers and enable it to login as root without using password.
