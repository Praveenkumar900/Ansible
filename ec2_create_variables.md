# In Ansible, Variables can be declared at 22 different locations/places
Eg1: /role/defaults/main.yaml --> type: t2.micro

This value we can refer in playbook as below:
instance_type: "{{ type }}"

Eg2: /role/vars/main.yaml --> type: t2.medium

This value we can refer in playbook as below:
instance_type: "{{ type }}"

Note: defaults has less priority than vars. SO, the Ec2 instance of "t2.medium" will be created

Eg3: We can pass variblaes as Env Varibales as below manually:

ansible-playbook -i inventory.ini ec2_create.yaml --vault-password-file vault.pass -e type=t2.micro

Eg4: We can directly declare Varibales in Playbook as well:

