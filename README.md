[![MIT License](https://raw.githubusercontent.com/roles-ansible/role_install-epel-release/master/.github/license.svg?sanitize=true)](https://github.com/roles-ansible/role_install-epel-release/blob/master/LICENSE) [![Ansible Galaxy](https://raw.githubusercontent.com/roles-ansible/role_install-epel-release/master/.github/galaxy.svg?sanitize=true)](https://galaxy.ansible.com/do1jlr/epel) [![Ansible check centos:latest](https://github.com/roles-ansible/role_install-epel-release/workflows/Ansible%20check%20centos:latest/badge.svg)](https://github.com/roles-ansible/role_install-epel-release/actions?query=workflow%3A%22Ansible+check+centos%3Alatest%22)

 role_install-epel-release
============================
Ansible role to install the Extra Packages for Enterprise Linux (EPEL) - Repository on RHEL and centos.

### What do we do here?
+ First we read the variables you configured and our default values.
+ If enabled *(default to false)*, we do a simple version-check that will validate that you never run a older version of this role after you run this role before.
+ We validate that the GPG key of the EPEL repo for your distribution release is installed and match the fingerprint in the config.
+ We install the epel repo from a remote URL.

### example useage of this role
You can either use this role via ansible galaxy or by downloading this role manually.

#### ansible galaxy: install this role
```bash
ansible-galaxy install do1jlr.epel
```

#### ansible-galaxy: example playbook
```yml
---
- name: install epel release
  hosts: srv01.example.com
  roles:
    - do1jlr.epel
```

#### manual download role
```bash
# download to your roles directory
git clone https://github.com/roles-ansible/role_install-epel-release.git
```

#### manual example playbook
```yaml
---
- name: Install epel release
  hosts: srv02.example.com
  tags:
   - epel
  vars:
    submodules_versioncheck: true
  roles:
    - role_install-epel-release
``` 

### variables and configuration

Here a our default values you can overwrite:
```yaml
# do we want a simple versionscheck? (true is recomended)
submodules_versioncheck: false

# epel repo
epel_repo:
  url: "https://dl.fedoraproject.org/pub/epel/epel-release-latest-{{ ansible_distribution_major_version }}.noarch.rpm"
  gpg_key_url: "https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-{{ ansible_distribution_major_version }}"
  gpg_key_path: "/etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-{{ ansible_distribution_major_version }}"
  fingerprint:
    '6': "8C3B E96A F230 9184 DA5C 0DAE 3B49 DF2A 0608 B895"
    '7': "91E9 7D7C 4A5E 96F1 7F3E 888F 6A2F AEA2 352C 64E5"
    '8': "94E2 79EB 8D8F 25B2 1810 ADF1 21EA 45AB 2F86 D6A1"
```

### Testing
This role is tested with [these github-action](https://github.com/search?q=topic%3Acentos+topic%3Acheck-ansible+topic%3Agithub-actions+org%3Aroles-ansible&type=Repositories) tests for different versions of centos. Linting is tested via travis-ci.
If you want to find out more about our tests, please have a look at the github marketplace.

| test status | Github Marketplace |
| :---------  | :----------------  |
| [![Travis Build Status](https://travis-ci.org/roles-ansible/role_install-epel-release.svg?branch=master)](https://travis-ci.org/roles-ansible/role_install-epel-release) | [.travis.yml](https://github.com/roles-ansible/role_install-epel-release/blob/master/.travis.yml) |
| [![Ansible check centos:latest](https://github.com/roles-ansible/role_install-epel-release/workflows/Ansible%20check%20centos:latest/badge.svg)](https://github.com/roles-ansible/role_install-epel-release/actions?query=workflow%3A%22Ansible+check+centos%3Alatest%22) | [ansible test with centos:latest](https://github.com/roles-ansible/role_install-epel-release/blob/master/.travis.yml) | [ansible test with centos latest](https://github.com/marketplace/actions/check-ansible-centos-latest) |
| [![Ansible check centos:centos8](https://github.com/roles-ansible/role_install-epel-release/workflows/Ansible%20check%20centos:centos8/badge.svg)](https://github.com/roles-ansible/role_install-epel-release/actions?query=workflow%3A%22Ansible+check+centos%3Acentos8%22) |  [ansible test with centos 8](https://github.com/marketplace/actions/check-ansible-centos-centos8) |
| [![Ansible check centos:centos7](https://github.com/roles-ansible/role_install-epel-release/workflows/Ansible%20check%20centos:centos7/badge.svg)](https://github.com/roles-ansible/role_install-epel-release/actions?query=workflow%3A%22Ansible+check+centos%3Acentos7%22) | [ansible test with centos 7](https://github.com/marketplace/actions/check-ansible-centos-centos7) |
| [![Ansible check centos:centos6](https://github.com/roles-ansible/role_install-epel-release/workflows/Ansible%20check%20centos:centos6/badge.svg)](https://github.com/roles-ansible/role_install-epel-release/actions?query=workflow%3A%22Ansible+check+centos%3Acentos6%22) | [ansible test with centos 6](https://github.com/marketplace/actions/check-ansible-centos-centos6) |
| [![Ansible Lint check](https://github.com/roles-ansible/role_install-epel-release/workflows/Ansible%20Lint%20check/badge.svg)](https://github.com/roles-ansible/role_install-epel-release/actions?query=workflow%3A%22Ansible+Lint+check%22) | [ansible linting test](https://github.com/marketplace/actions/ansible-lint) |
