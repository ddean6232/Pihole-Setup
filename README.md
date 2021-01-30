# Pihole-Setup

Pi-Hole is an awesome service to run in your house. It keeps ads from loading on every device, and will run on any Raspberry Pi, Docker container or virtual machine you'd like. But did you know it can do SO much more than just block ads? You can also completely bypass 3rd party DNS servers like 8.8.8.8, 1.1.1.1, 208.67. 222.222, or the ones ran by your ISP.


Installation Steps  

Install Ubuntu Server 20.04 (https://ubuntu.com/download/server)  
Install Pi-Hole - `sudo curl -sSL https://install.pi-hole.net | bash`  
Set the Web Admin Password - `pihole -a -p [password]`  
Install Unbound DNS - `sudo apt install unbound`  
Create Unbound Configuration File - `sudo nano /etc/unbound/unbound.conf.d/pi-hole.conf`  
Copy example config - https://docs.pi-hole.net/guides/dns/unbound/  
Restart Unbound to apply Configuration - `sudo service unbound restart`  
Disable Forwarding DNS in PiHole  
Set Custom DNS in PiHole - 127.0.0.1#5335  
