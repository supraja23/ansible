# CFGAAS

This project involves the configuration as a service (CFGaaS) environment using Ansible.

Configuring roles and playbooks that are part of AMaaS (Artifactory as a service) project. 

## Inventories
Remote hosts or grouping of host can be setup at Inventories folder. (This can be sourced to AWX tower for deployment)

## Role Variables
Defined in roles/../vars. These variables can be set in vars folder or externally using playbook. 
A general good practice is to define them in vars folder

## Dependencies
None.

## How it works

Example of how to use this role:

    - hosts: servers
      roles:
         - { role: artifactory }
         
    - hosts: your-servers
      roles:
        - { role: java, java_packages: java-11-openjdk}
