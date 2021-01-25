
![Lint Ansible Roles](https://github.com/tenantcloud/ansible-role-elk-common/workflows/Lint%20Ansible%20Roles/badge.svg)

tenantcloud.elk_common
=========

Ansible common role for setup nginx, change hostname. This role include in default terraform scenario for auto-deploy new server.

To increase maximum shards insert next code in Dev Tools in Kibana:
```bash
PUT _cluster/settings 
{ "persistent": { "cluster.max_shards_per_node": "30000" } }
``` 


Requirements
------------

ELK Stack, Elastalert, ReadOnlyRest

Role Variables
--------------

elk_hostname: elk.tenants.co
Hostname ELK Stack server

Dependencies
------------

  - geerlingguy.java
  - tenantcloud.elasticsearch
  - tenantcloud.kibana
  - tenantcloud.logstash
  - tenantcloud.ansible_role_elastalert
  - tenantcloud.ansible_role_auth_elk
  - tenantcloud.ansible_role_readonlyrest

Example Playbook
----------------

```yaml
  - hosts: localhost
    vars:
      elk_hostname: elk.tenants.co
    become: yes
    roles:
      - tenantcloud.elk_common
```

License
-------

BSD

Author Information
------------------

TenantCloud DevOps Team
