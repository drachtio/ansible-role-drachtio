# ansible-role-drachtio

This is an ansible role for installing a [drachtio server](https://github.com/davehorton/drachtio-server). 

## Role variables

The sip port(s) that drachtio is listening on
```
drachtio_ports: "5060"  # use comma-separated if multiple ports
```

## Example playbook
```
---
- hosts: all
  roles:
    - ansible-role-fail2ban-drachtio
  become: yes
```
