# Ansible Role: Heroku Toolbelt

[![Travis
CI](http://img.shields.io/travis/pablocrivella/ansible-role-heroku-toolbelt.svg?style=flat)](http://travis-ci.org/pablocrivella/ansible-role-heroku-toolbelt)
[![test-suite](http://img.shields.io/badge/ansible--roles--specs-ansible--role--rbenv-blue.svg?style=flat)](https://github.com/pablocrivella/ansible-roles-specs/tree/master/ansible-role-heroku-toolbelt/)
[![Ansible
Galaxy](http://img.shields.io/badge/galaxy-pablocrivella.heroku--toolbelt-660198.svg?style=flat)](https://galaxy.ansible.com/list#/roles/3123)

Role to install rbenv and multiple ruby versions.

## Requirements

Tested with Ansible 1.8.4.

## Role Variables

```yaml
---
heroku_toolbelt_users:
  - name: vagrant

heroku_toolbelt_plugins:
  - git://github.com/heroku/heroku-pg-extras.git
  - git://github.com/heroku/manager-cli.git
  - git://github.com/ddollar/heroku-config.git
  - git://github.com/ddollar/heroku-accounts.git
```

## Dependencies

None

## Example Playbook

```yaml
- hosts: ruby-devbox
  roles:
    - pablocrivella.heroku-toolbelt
```

## License

MIT

## Author Information

Pablo Crivella Backend Engineer @ NobelBiz.
