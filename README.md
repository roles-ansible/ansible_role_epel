[![MIT License](https://raw.githubusercontent.com/roles-ansible/role_install-epel-release/master/.github/license.svg?sanitize=true)](https://github.com/roles-ansible/role_install-epel-release/blob/master/LICENSE)
[![Ansible Galaxy](https://raw.githubusercontent.com/roles-ansible/role_install-epel-release/master/.github/galaxy.svg?sanitize=true)](https://galaxy.ansible.com/do1jlr/epel)

 role_install-epel-release
============================
Ansible role to install the Extra Packages for Enterprise Linux (EPEL) - Repository on RHEL and centos.

### Testing
This role is tested with [these github-action](https://github.com/search?q=topic%3Acentos+topic%3Acheck-ansible+topic%3Agithub-actions+org%3Aroles-ansible&type=Repositories) tests for different versions of centos. Linting is tested via travis-ci.
If you want to find out more about our tests, please have a look at the github marketplace.

| test status | Github Marketplace |
| :---------: | :----------------: |
| [![Travis Build Status](https://travis-ci.org/DO1JLR/role_install-epel-release.svg?branch=master)](https://travis-ci.org/DO1JLR/role_install-epel-release) | [.travis.yml](https://github.com/roles-ansible/role_install-epel-release/blob/master/.travis.yml) |
[![Ansible check centos:latest](https://github.com/roles-ansible/role_install-epel-release/workflows/Ansible%20check%20centos:latest/badge.svg)](https://github.com/roles-ansible/role_install-epel-release/actions?query=workflow%3A%22Ansible+check+centos%3Alatest%22) | [ansible test with centos:latest](https://github.com/roles-ansible/role_install-epel-release/blob/master/.travis.yml) | [ansible test with centos latest](https://github.com/marketplace/actions/check-ansible-centos-latest) |
| [![Ansible check centos:centos8](https://github.com/roles-ansible/role_install-epel-release/workflows/Ansible%20check%20centos:centos8/badge.svg)](https://github.com/roles-ansible/role_install-epel-release/actions?query=workflow%3A%22Ansible+check+centos%3Acentos8%22) |  [ansible test with centos 8](https://github.com/marketplace/actions/check-ansible-centos-centos8) |
| [![Ansible check centos:centos7](https://github.com/roles-ansible/role_install-epel-release/workflows/Ansible%20check%20centos:centos7/badge.svg)](https://github.com/roles-ansible/role_install-epel-release/actions?query=workflow%3A%22Ansible+check+centos%3Acentos7%22) | [ansible test with centos 7](https://github.com/marketplace/actions/check-ansible-centos-centos7) |
| [![Ansible check centos:centos6](https://github.com/roles-ansible/role_install-epel-release/workflows/Ansible%20check%20centos:centos6/badge.svg)](https://github.com/roles-ansible/role_install-epel-release/actions?query=workflow%3A%22Ansible+check+centos%3Acentos6%22) | [ansible test with centos 6](https://github.com/marketplace/actions/check-ansible-centos-centos6) |
| [![Ansible Lint check](https://github.com/roles-ansible/role_install-epel-release/workflows/Ansible%20Lint%20check/badge.svg)](https://github.com/roles-ansible/role_install-epel-release/actions?query=workflow%3A%22Ansible+Lint+check%22) | [ansible linting test](https://github.com/marketplace/actions/ansible-lint) |




```
WORK IN PROGRESS

missing:
- os detection (RHEL)
- docs

working:
- epel install on centos 7
- github-actions
- vars
```
