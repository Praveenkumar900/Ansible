Ansible-Galaxy → We have thousands of Ansible Roles. 
Scenario:
If we are given a task of installing and configuring Docker. If the Manage Nodes are using different Linux flavours [Redhat, Debian, Ubuntu, Alpine, Windows]. 
Here, the complexity of Ansible Playbook will be high as we have to consider all these Linux Flavours in order to install Docker on all the Manage Nodes.

Ansible Galaxy > Search for Docker > 

#To install an existing role from Ansible Galaxy on our Control Node
ansible-galaxy role install lean_delivery.jenkins   #Jenkins installation and configuration
