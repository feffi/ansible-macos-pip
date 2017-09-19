# ansible-macos-pip
Ansible role to manage python/pip and packages.

[![Build Status](https://img.shields.io/travis/feffi/ansible-macos-pip.svg)](https://travis-ci.org/feffi/ansible-macos-pip) [![Github All Releases](https://img.shields.io/github/downloads/feffi/ansible-macos-pip/total.svg)](https://github.com/feffi/ansible-macos-pip) [![GitHub forks](https://img.shields.io/github/forks/feffi/ansible-macos-pip.svg?style=social&label=Fork)](https://github.com/feffi/ansible-macos-pip) [![GitHub stars](https://img.shields.io/github/stars/feffi/ansible-macos-pip.svg?style=social&label=Star)](https://github.com/feffi/ansible-macos-pip) [![GitHub watchers](https://img.shields.io/github/watchers/feffi/ansible-macos-pip.svg?style=social&label=Watch)](https://github.com/feffi/ansible-macos-pip) [![Twitter Follow](https://img.shields.io/twitter/follow/feffi1.svg?style=social&label=Follow)](https://twitter.com/feffi1) [![License](http://img.shields.io/:license-mit-blue.svg)](https://github.com/feffi/ansible-macos-pip/blob/master/LICENSE)

## Requirements
- Ansible 2.3

### ansible.cfg
```
hash_behaviour = merge
```

## Install
Just add the role to your ``requirements.yml`` file:
```yaml
- src: https://github.com/feffi/ansible-macos-pip.git
  name: feffi.macos-pip
```

## Role Variables
All role based variables are listed below, along with default values:

```yaml
macos_pip:
  # Packages to install via python pip
  packages: []
```

## Dependencies
None.

## Example Playbook

```yaml
    - hosts: all
      vars:
        macos_pip:
          packages: []
      roles:
        - { role: feffi.macos-pip }
```
Or with local parameters:

```yaml
    - hosts: all
      roles:
        - { role: feffi.macos-pip,
            macos_pip: {
              packages: []
            }
          }
```
