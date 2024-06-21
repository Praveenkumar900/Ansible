# In Ansible, Variables can be declared at 22 different locations/places
Eg1: /role/defaults/main.yaml --> type: t2.micro

This value we can refer in playbook as below:
instance_type: "{{ type }}"

Eg2: /role/vars/main.yaml --> type: t2.medium

This value we can refer in playbook as below:
instance_type: "{{ type }}"
