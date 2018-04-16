ansible-stolon-role

example for role addition

```yaml
- hosts: postgresql-stolon
  name: postgresql-stolon
  become: true
  roles:
    - role: ansible-postgres-simple
    - role: ansible-etcd
    - role: ansible-stolon
  tasks:

  vars:
    postgresql_version: 9.5
#    stolon_init: true
#    stolon_init_mode: new
#    stolon_postgres_port: 6432

  tags:
    - postgresql-stolon
```
