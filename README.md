Ansible role for setup common ELK Stack tasks
=========

Common ELK Stack role for install logstash patterns, change default nginx config file. This role include in default terraform scenario for auto-deploy new server.

-------

For manual installation this role:

```ansible-galaxy install tenantcloud.ansible_role_elk_common```

Add this role name to playbook and run:

```cd /tmp/.ansible/ && ansible-playbook playbook-name.yml```

-------

Variable included in this role:

{{ elk_url }} - url for ELK Stack server

-------

Sample playbook-name.yml

- hosts: localhost
  vars:
    elk_url: https://elk.tc.cloud
  become: yes
  roles:
    - ansible-role-elk-common
