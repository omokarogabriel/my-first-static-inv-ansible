***Ansible Static Inventory Setup***

*inventory.yml*
```yml
webservers:  #name of the host (grouped)
  hosts:
    54.164.102.89:  #List of the host ip
      ansible_user: ubuntu  # Host user
      ansible_ssh_private_key_file: /home/omokaro/AwsKey  #file path to the private key on the control node, it must tally with the ec2 instance key-name

    3.95.187.49:
      ansible_user: ubuntu
      ansible_ssh_private_key_file: /home/omokaro/AwsKey
```

*ansible.cfg*

- [defaults]
- inventory = ./inventory.ini
- remote_user = ubuntu
- private_key_file = /home/omokaro/AwsKey
- host_key_checking = False
- timeout = 30

*here is the inventory.ini*
- [webservers]
- 54.164.102.89 ansible_user=ubuntu ansible_ssh_private_key_file=/home/omokaro/AwsKey
- 3.95.187.49 ansible_user=ubuntu ansible_ssh_private_key_file=/home/omokaro/AwsKey

*Note: There are all in a folder*