Milestone 1: Create MHN Admin VM

Created the MHN admin  VM via the google cloud provider. The following attributes were used:
1.	Ubuntu 14.04
2.	Micro memory, (0.6 GB)
3.	HTTP and HTTPS traffic allowed (port 80, port 443)
4.	TCP ports 3000 and 1000 need to be open to allow incoming (AKA ingress) traffic.
5.	Make sure the VM can be accessed through SSH

 
Set the Firewall rule. 
 

Milestone 2: Install the MHN admin application

SSH into the MHN-admin and enter the following commands in order to install the MHN admin application. 

1.	sudo apt-get update (update)
2.	sudo apt-get install git -y (install git)
3.	cd /opt
4.	ls
5.	sudo git clone http://github.com/threatstream /mhn (clone the mhn admin application)
6.	cd mhn
7.	sudo ./install.sh (This step will take time 15-20 mins)

Milestone 3: Create an MHN Honeypot VM


You will now be able to use the external IP address in the browser and login using the credentials (email and password) used in the previous step.

 

Milestone 4: Install the honeypot application

Login to the MHN terminal. Launched two different firewalls:
1.	Ubuntu with Dionaea
2.	Ubuntu with shockpot

Milestone 5: Was not able to download the data from the honeypots
