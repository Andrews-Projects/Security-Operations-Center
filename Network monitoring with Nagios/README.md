# Nagios Network Analyzer

In this section I plan to implement Nagios,the network monitoring tool, to monitor the 3 Ubuntu based servers created
in the 1st project to learn Ansible & Vagrant.   [Link to 1st project](https://github.com/Andrews-Projects/Ansible-Vagrant-infrastructure-development-and-deployment)

As per the installation instructions in their official documentation,Nagios should be installed on a fresh system to avoid failure of existing sytems due 
to the modification it makes to the system.   [View Installation Guide](https://assets.nagios.com/downloads/nagios-network-analyzer/docs/Network_Analyzer_Manual_Installation_Instructions.pdf)

The architecture is abit crazy but im simply using the resources at my disposal

My architecture[Drawn image of setup]()


I set-up an Ubuntu Server on the VmWare workstation & install Nagios

Working on Ubuntu server I hasd to be root. 

└──╼ $ sudo -i

└──╼ $ curl https://assets.nagios.com/downloads/nagios-network-analyzer/install.sh | sh
