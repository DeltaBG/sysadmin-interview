# Instructions
* Follow the tasks by beginning from task 1.
* You can skip task-2 if you are not familiar with Ansible. All other VMs must be configured manually if that is the case.

## Requirements
* All configured tasks and services must survive a reboot.
* All Ansible inventory files, variables, roles and playbooks must be present in the directory /home/ansible/automation/.
* Hosts web1.example.com, web2.example.com and db.example.com should not be accessed directly from the Internet.

## Expected end result
Point example.com to the public IP which you assigned to lb.example.com. If you have completed all the tasks successfully, you should see the default Wordpress "Hello world" page.
