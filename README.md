# AWS Magento AMI

This repository builds a base Magento AMI that installs all the fundamental packages to run a Magento application.

## Why

## Source Code structure

```bash
├── ansible
├── roles
|   ├── common
|       └── tasks
|            └── main.yaml
|   ├── magento
|       └── tasks
|            └── main.yaml
|       └── vars
|            └── main.yaml
|   ├── mysql
|       └── tasks
|            └── main.yaml
|   ├── nginx
|       └── tasks
|            └── main.yaml
|   ├── php
|       └── files
|            └── php.ini
|       └── tasks
|            └── main.yaml
```

## Built with

* [Packer](https://www.packer.io/)
* [Ansible](https://www.ansible.com/)
* Shell
