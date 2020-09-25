# Install and configure a KVM host

## Scenario
You are provided with a headless server, installed with a minimal CentOS OS. The server is provided with with a public /29 public network. The server already has a pre-configured network interface with a public IP assigned from the same network.

## Tasks
* Check if the host has virtualization capabilities.
* Install libvirt and all of its required packages. Start the service and enable it on boot.
* Verify your KVM installation and check if the appropriate kernel module is present.
* Create 4 guest VMs. Their requirements are as follows:
	*. Linux distro of your choice. Use the most recent version available at the moment.
	*. The VMs hostnames should be: lb.example.com, web1.example.com, web2.example.com and db.example.com.
	*. Each VM should have 1 vCPU, 2GB RAM and 10GB disk.
	*. Use the default libvirt network bridge since you will need outbound Internet access on each machine.
* You are not limited on how you can install the guest VMs - you can use either libirt's VNC, virt-manager or some other tool.
** TIP:** You can clone an already installed VM in order to save time and avoid installing each of the VMs every time.
