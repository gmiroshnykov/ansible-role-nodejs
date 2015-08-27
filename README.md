ansible-role-nodejs
===================

This Ansible role installs Node.js

## Usage

You can call this role from a playbook:

```
---
- hosts: webservers

  roles:
    - laggyluke.nodejs
```

or use it as a dependecy of another role, eg. in `roles/ci-server/meta/main.yml`:

```
---
dependencies:
  - { role: laggyluke.nodejs }
```

## Variables

Available variables:

```
nodejs.devel: false                         # Install latest dev release if true, stable release if false
nodejs.add_node_modules_bin_to_path: false  # Add `./node_modules/.bin` to $PATH if true
nodejs.npmrc: {}                            # Custom `~/.npmrc`
```

By default this role does what it says on the cover: simply installs Node.js so you have access to `node` and `npm`.
