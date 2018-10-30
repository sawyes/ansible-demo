# install 

on server

```
yum update
yum -y install ansible
```


# usage

```
ansible-playbook zabbix_agent.yml
```

* -i, --inventory, --inventory-file

default: /etc/ansible/hosts

```
ansible-playbook -i inventory/zabbix_agent.yml zabbix_agent.yml
```

# doc

```
ansible-doc hostname
```

