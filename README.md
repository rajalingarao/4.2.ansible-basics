# How to run ansible playbook:
```
ansible-playbook -i inventory.ini -e ansible_user=ec2-user -e ansible_password=DevOps321 01-ping.yaml 
```
```
ansible-playbook -i inventory.ini -e ansible_user=ec2-user -e ansible_password=DevOps321 02-nginx.yaml 
```

```
ansible-playbook -i inventory.ini -e ansible_user=ec2-user -e ansible_password=DevOps321 03-multi-play.yaml 
```

```
ansible-playbook -i inventory.ini -e ansible_user=ec2-user -e ansible_password=DevOps321 -e PERSON=Ramesh -e WISHES=Morning 09-vars-args.yaml
```
```
ansible-playbook -i inventory.ini -e "PERSON=Ramesh WISHES=Morning" -e ansible_user=ec2-user -e ansible_password=DevOps321 09-vars-args.yaml
```

# The playbook executed on the remote host:

```
```
ansible-playbook -i inventory.ini  -e ansible_user=ec2-user -e ansible_password=DevOps321 18-command-vs-shell.yaml
```
ansible_agent.lithesh.shop
```

* not on your Ansible control node (172.31.82.28).
```
cd /tmp
ls -l
```
* You should see:

shell.txt

```
* Most likely:
shell.txt contains the message
command.txt was not created properly because > is not interpreted by command
```

* Proper way to validate file creation with command

*Use safe commands only:
```
- name: create file using command
  ansible.builtin.command: touch /tmp/test.txt
```
Then validate:
```
ls -l /tmp/test.txt
```
or inside Ansible:
```
- name: check file exists
  ansible.builtin.command: ls -l /tmp/test.txt
```

