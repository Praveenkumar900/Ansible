Ansible-Galaxy → We have thousands of Ansible Roles. 
Scenario:
If we are given a task of installing and configuring Docker. If the Manage Nodes are using different Linux flavours [Redhat, Debian, Ubuntu, Alpine, Windows]. 
Here, the complexity of Ansible Playbook will be high as we have to consider all these Linux Flavours in order to install Docker on all the Manage Nodes.

Ansible Galaxy > Search for Docker > 

#To install an existing role from Ansible Galaxy on our Control Node
ansible-galaxy role install lean_delivery.jenkins   #Jenkins installation and configuration

Setup Vault:

Create a password for vault
https://e2.udemymail.com/ls/click?upn=u001.nWn-2BtWPikR2ffCZ57VsEbFNaoCfjxqMpCE-2FtmiaJKELu9CLC0Z1ugYw8ml6E4wXKJ-2FBivu1xMq0dEMURkcCv4f5cEjIPBnw0lfbefcaW3r-2BW-2F7Bg-2FZQ2O4TLwREwaRVV6rUUqRQciFTfSuJBwKWerPnyrLL5-2F-2FKCmZidCfmN7hfQalZDHWw-2FZYnxaM9Qd89mdlAe2SOQ6AnpPICG9AhwcXRTWkft2KwMgCYF-2Bfp2tIMKSQByvG9scXFFaMTWuyAqXcryF82SXqZvCKc1X6i-2BJvhXuj12w7-2BTKIbU6u7MmFo-3D0Xxk_uXIYe6s2xoYdJDWeVkM19LjAhi9JvOZMbwu-2F6q7R9sTOB6ldNiMzpLZPq9sFT512q79YULZMsKbIfrd2zXJPaY6cEPzOdiZ8SvcbCQDIz4Odn1ZEjxLo1qT3HBrHxhq-2BM-2BTyS-2Bfagnifc4fGRJpkCTZn8BU7Z0eTAilB3WkIGa48b3sVPYon2o3Cl-2F8unuvPWdHrl7xtR-2BaK4ZRD0G-2B4DBKInDZl5ob-2BwFZeJvG-2B2v2G6Ftlm2i8Ljpi93prX1m99pVlp1AmjiaFSM26kVl6l4VZGZs5mrT1TrmagPHTx5eyMNTIIetdI1yVCZq6a8PadRbs-2B8NUU3D5ziLjNbJhmtDUPm95Izz6mO6xlAXGAGFDVTyxKWOg5UKXQqIrsZFC 
openssl rand -base64 2048 > vault.pass

Add your AWS credentials using the below vault command

ansible-vault create group_vars/all/pass.yml --vault-password-file vault.pass

In this file, add AWS Access_Key and Secret_Key
