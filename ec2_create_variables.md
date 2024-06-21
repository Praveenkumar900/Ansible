# In Ansible, Variables can be declared at 22 different locations/places
/role/defaults/main.yaml --> type: t2.micro
This value we can refer in playbook as below:
instance_type: "{{ type }}"
