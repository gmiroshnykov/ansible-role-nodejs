#nodejs - forever - initd-forever
================================

An Ansible role that installs nodejs and runs default or your application on Ubuntu 12.04 - 15.10

- If you just want to test Node, this role got you covered, it comes with a simple Hello World app
- NodeJS is added as service (using NPM packages) allowing you to service start|stop it



#### Role Variables

Available variables are listed below, along with default values:

####Default Node.js bin path
nodejs:
  add_node_modules_bin_to_path: false
  npm: {}

####Change when deploying to production
node_env: 'development'

####Default root
nodeapp_chdir: '/'

####Default Hello world app that comes with role, add your own apps here
nodeapps:
  - { id: 'nodeapp', path: '/home/nodeapp/', app: 'server.js' }

####Required global packages to create and run base application feel free to add your own packages here
nodeapp_npm:
  - forever
  - initd-forever


#### License

MIT
