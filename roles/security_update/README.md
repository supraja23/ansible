Security Update Role
=========

Please run this playbook carefully!
Run job template AWX adding to limit ONE cluster to job


Role Variables
--------------
reboot_required: no(default) #Initial state of variable that changes if reboot is required 

update: #Initiated variable to debug output later


Example Playbook
----------------

- hosts: "{{ ansible_limit | default('no_hosts')}}"
  gather_facts: False
  serial: 2 #Number of hosts in a cluster
  any_errors_fatal: true #Stop play for ALL hosts in a cluster if any task fails on any host
  roles:
    - role: security_update
      tags: security_update


Author Information
------------------

Alexey.Parkhomenko@dell.com