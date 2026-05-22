# How to run ansible playbook:

```
ansible-playbook -i inventory.ini -e ansible_user=ec2-user -e ansible_password=DevOps321 01-ping.yaml 
```

```
ansible-playbook -i inventory.ini -e ansible_user=ec2-user -e ansible_password=DevOps321 -e PERSON=Ramesh -e WISHES=Morning 09-vars-args.yaml
```

```
ansible-playbook -i inventory.ini -e "PERSON=Ramesh WISHES=Morning" -e ansible_user=ec2-user -e ansible_password=DevOps321 09-vars-args.yaml
```


