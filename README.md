rkhunter role
==============

Description
-----------

This role install, configure and run rkhunter.

Defaults
------------

Ensure that rkhunter is enabled to run daily
```YAML
rkhunter_cron: yes
rkhunter_config: yes
rkhunter_logrotate: yes
rkhunter_run: yes
```

Example
-------

Playbook: Rkhunter Hardening

```YAML
---
- name: "Security: Linux Rootkit Check - Rkhunter"
  hosts: linux
  become: true

  tasks:
    - name: "victorock.rkhunter"
      include_role:
        name: victorock.rkhunter
        tasks_from: run
```

Authors
-------

Victor da Costa
