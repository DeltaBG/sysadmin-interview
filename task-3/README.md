# Configure lb1.example.com

## Scenario
The VM you are configuring will be used as a loadbalancer. The software which you will be using in order to achieve that is HAProxy.

## Tasks
* Assign a static private IP address from the same default virbr0 network, assigned on the host server.
* Assign another static IP address to the lb.example.com VM. The address must be from the same /29 network which you are already provided with. 
* Install HAProxy and enable it to start on boot.
* Configure HAProxy with the following requirements:
	* Configure 1 frontend. Use public IP which you have already configured. Bind it to port 80. The frontend's default_backend should be the backends described in the next subtask.
	* Configure 1 backend with 2 servers present in it. The servers addresses should be the ones which used for configuring web1.example.com and web2.example.com.
	* The preferred balance algorythm should be "roundrobin".

### Bonus tasks
* Install and configure HAProxy using Ansible. You can use your own role/playbook or ready-made role from Ansible Galaxy. These tasks must be done from user "ansible".
