# Install and configure Nginx + PHP-FPM

## Scenario
You will be installing Nginx and PHP-FPM. They must be configured in order to serve a default Wordpress installation. 

## Tasks
Configure web1.example.com and web2.example.com as follows:
* Each host must have Nginx and PHP-FPM installed and configured to start on boot. PHP version does not matter, use 7.3 if you are not sure what to use.
* Create a new user called "wordpress".
* Configure new PHP-FPM pool. Configure it using UNIX or TCP socket. Use the user "wordpress" when configuring PHP-FPM pool.
* Configure the following options in the php.ini file on each host:
	* upload_max_filesize = 32M
	* post_max_size = 16M
	* memory_limit = 64M
* Nginx must be configured to use the PHP-FPM pool configured above.
* Nginx must have a server block configured with the following requirements:
	* Configure server_name as example.com.
	* Create /home/wordpress/public_html and use it as document root

## Bonus tasks
* Configure and install Nginx/PHP-FPM using Ansible. You can use your own role/playbook or ready-made role from Ansible Galaxy. These tasks must be done from user "ansible".
