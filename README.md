nodejs, Forever, upstart
========================
# README.md

An Ansible role that installs nodejs and runs default or your application on Ubuntu 12.04 - 15.10

- Added npm install of forever (more packages can be added in vars/default
- NodeJS is added as service allowing you to service start|stop it
- if the node app as defined in vars(defaults) does not exist a simple server.js is put in it's place


#### Role Variables

Available variables are listed below, along with default values:

####Default Node.js bin path
nodejs:
  add_node_modules_bin_to_path: false
  npm####: {}

####When c####ange when deploying to production
node_env: 'development'

####Default####root
nodeapp_chdir: '/'

####Default Hell#### world app that comes with role, add your own apps here
nodeapps:
  - { id: 'nodeapp', path: '/home/nodeapp/', app: 'server.js' }

####Required global packages to create and run base application feel free to add your own packages here
nodeapp_npm:

#### forever
  - initd-forever


#### License

MIT