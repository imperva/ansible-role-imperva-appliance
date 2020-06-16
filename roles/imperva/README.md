Role Name
=========

The Imperva role can be used to upgrade installed Imperva gateways and MXs.

Requirements
------------

You will need to have an active Imperva support contract to to download the required patches.  

You will also need an ansible capable user created on each system (the default admin user will NOT work for this - it uses a restricted shell that ansible doesn't like.  See ansible-role-imperva-appliance/README.md for details and how to create.

Role Variables
--------------
See var/main.yml

Dependencies
------------
See ansible-role-imperva-appliance/extension/setup/python_requirements.txt

Example Playbook
----------------
See ansible-role-imperva-appliance/playbooks/common.yml

License
-------

MIT

Author Information
------------------

Imperva Global Solutions Architecture team
