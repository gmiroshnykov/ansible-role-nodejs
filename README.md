nodejs, Forever, upstart
========================

This Ansible role installs Node.JS.

- Added npm install of forever (more packages can be added in vars/default
- Created upstart conf file and copy it to /etc/init
- added default values that can be overridden from playbook.yml
- if the node app as defined in vars(defaults) does not exist a simple server.js is put in it's place
