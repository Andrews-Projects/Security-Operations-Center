# Nagios Network Monitor

In this section I plan to implement Nagios,the network monitoring tool, to monitor the 3 Ubuntu based servers created
in the 1st project to learn Ansible & Vagrant.   [Link to 1st project](https://github.com/Andrews-Projects/Ansible-Vagrant-infrastructure-development-and-deployment)

As per the installation instructions in their official documentation,Nagios should be installed on a fresh system to avoid failure of existing sytems due 
to the modification it makes to the system.   [View Installation Guide](https://assets.nagios.com/downloads/nagios-network-analyzer/docs/Network_Analyzer_Manual_Installation_Instructions.pdf)

The architecture is abit crazy but i'm simply using the resources at my disposal as of the time of this writing.

## My architecture: 

![Image](https://github.com/Andrews-Projects/Security-Operations-Center/blob/master/Network%20monitoring%20with%20Nagios/images/nagios.png)


I set-up an Ubuntu Server on the VmWare workstation & install Nagios

Working on Ubuntu server I hasd to be root. 

└──╼ $ sudo -i

└──╼ $ curl https://assets.nagios.com/downloads/nagios-network-analyzer/install.sh | sh

The next step after finishing installation is to visit:

http://172.x.x.x/nagiosna/

This is the home Nagios home page to create an account & then login
![Nagios_Login_Page](https://github.com/Andrews-Projects/Security-Operations-Center/blob/master/Network%20monitoring%20with%20Nagios/images/nagios_login.png)

## Next Step: 

Create Source,this is the source of the network traffic from your configured online servers.

![Create source page](https://github.com/Andrews-Projects/Security-Operations-Center/blob/master/Network%20monitoring%20with%20Nagios/images/create%20source.png)

After adding my 2 Ubuntu Servers this is the final result viewed from the Nagios home page.

![Sources](https://github.com/Andrews-Projects/Security-Operations-Center/blob/master/Network%20monitoring%20with%20Nagios/images/nagiospanel.png)

## Final Overview

After all has been set up,Ubuntu Nagios server ---> Ubuntu Server 1 & Ubuntu Server 2

![screenshot](https://github.com/Andrews-Projects/Security-Operations-Center/blob/master/Network%20monitoring%20with%20Nagios/images/allactivity.png)


### To liven things up I wanted to see if it was possble to perform a **ping flood attack** on Server 2 from Server 1
### i.e a Denial of Service attack.And see if i will be able to capture the traffic through Nagios.

└──╼ $ ping 172.16.x.x -l 65500 -w 1 -n 1  

But it wasnt successful and i go an error message 

ping:packet size 65500 is too large. Maximum is 65467,So I tried to reduce its size to 60000.Ping flooding didnt work.But it was fun


### Set-up is complete,Nagios has been set-up,2 servers are up and have been connected to it,communication has been established.

# This is it for Nagios Network Monitor implementation.





