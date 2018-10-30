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

>[info] specify inventory host path or comma separated host list. --inventory-file is deprecated

default: /etc/ansible/hosts

```
ansible-playbook -i inventory/zabbix_agent.yml zabbix_agent.yml
```

# doc

to get how to use a module

```
ansible-doc hostname
```

# playbook

what happen running `ansible-playbook -i inventory/zabbix_agent.yml zabbix_agent.yml`

## start

* who (client hosts)

define in `zabbix_agent.yml` ===> `hosts: zabbix_agent`

who is zabbix_agent hosts ===> inventory `zabbix_agent`

inventory/zabbix_agent.yml such as:

```
[zabbix_agent]
x.x.x.236	hostname=test-server-1 meta=spider
```

* play what

define in `zabbix_agent.yml` ===> `hosts: zabbix_agent`

```
  roles:
  - zabbix_agent
  - base
```

there many roles define in roles folder what you want to run

each roles folder `tasks` is important that define to do what


