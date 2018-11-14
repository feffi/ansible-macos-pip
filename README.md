# ansible-pip

Ansible role to manage python/pip and packages.

[![Build Status](https://img.shields.io/travis/feffi/ansible-pip.svg)](https://travis-ci.org/feffi/ansible-pip) [![Github All Releases](https://img.shields.io/github/downloads/feffi/ansible-pip/total.svg)](https://github.com/feffi/ansible-pip) [![GitHub forks](https://img.shields.io/github/forks/feffi/ansible-pip.svg?style=social&label=Fork)](https://github.com/feffi/ansible-pip) [![GitHub stars](https://img.shields.io/github/stars/feffi/ansible-pip.svg?style=social&label=Star)](https://github.com/feffi/ansible-pip) [![GitHub watchers](https://img.shields.io/github/watchers/feffi/ansible-pip.svg?style=social&label=Watch)](https://github.com/feffi/ansible-pip) [![Twitter Follow](https://img.shields.io/twitter/follow/feffi1.svg?style=social&label=Follow)](https://twitter.com/feffi1) [![License](http://img.shields.io/:license-mit-blue.svg)](https://github.com/feffi/ansible-pip/blob/master/LICENSE)

## Requirements

- Ansible 2.3
- Python >= 2.7

### ansible.cfg

```yaml
hash_behaviour = merge
```

## Install

Just add the role to your ``requirements.yml`` file:

```yaml
- src: https://github.com/feffi/ansible-pip.git
  name: ansible-pip
```

## Role Variables

All role based variables are listed below, along with default values:

```yaml
ansible_pip:
  # Packages to install via python pip
  packages: []
```

## Dependencies

None.

## Example Playbook

```yaml
    - hosts: all
      vars:
        ansible_pip:
          packages: []
      roles:
        - { role: ansible-pip }
```

Or with local parameters:

```yaml
    - hosts: all
      roles:
        - { role: ansible-pip,
            ansible_pip: {
              packages: []
            }
          }
```
