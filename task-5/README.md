# Install and configure MariaDB

## Scenario
You will be installing and configuring MariaDB on the database host. Clients from PHP-FPM hosts should be able to connect to this MySQL server. 

## Tasks
* Install MariaDB and enable it to start on boot. MariaDB version does not matter, use 10.1+ if you are not sure.
* Create empty database called "wordpress"
* Create necessary users called "wordpress_user". Keep in mind that these users should allow database connections from the web1.example.com and web2.example.com hosts.
* Set the following configuration options for the newly installed MySQL server:
	* innodb_buffer_size = 128M
	* max_allowed_packet = 16M 

## Bonus tasks
* Configure and install MariaDB using Ansible. You can use your own role/playbook or ready-made role from Ansible Galaxy. These tasks must be done from user "ansible".
