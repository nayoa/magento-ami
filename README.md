# AWS Magento AMI

This repository builds a base Magento AMI that installs all the fundamental packages to run a Magento application.

## Why

The idea is to install as much as possible on the base Magento AMI that is not unique to an evironment. This AMI is then used in the [magento_service](https://gitlab.com/evesleep/infrastructure/magento/magento-service) repo to spin up and configure a new environment in AWS. This will reduce the amount of time to spin up a new instance when autoscaling.

## Source Code structure

```bash
├── magento_ami
    ├── ansible/
        ├── roles/
            ├── common/
            |    └── tasks/
            |         └── main.yaml
            ├── redis/
            |   └── tasks/
            |        └── main.yaml
            ├── magento/
            |    └── tasks/
            |         └── main.yaml
            |    └── vars
            |         └── main.yaml
            ├── mysql/
            |   └── tasks/
            |        └── main.yaml
            ├── nginx/
            |   └── tasks/
            |        └── main.yaml
            ├── php/
            |   └── tasks/
            |        └── main.yaml
    ├── .gitignore
    ├── .gitlab-ci.yml
    ├── README.md
    ├── packer.json
```

## Built with

* [Packer](https://www.packer.io/)
* [Ansible](https://www.ansible.com/)
* Shell
