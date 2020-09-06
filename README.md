# My-One-Page-CV-Deployment

## Deployment Setup

Create a 'var_secret' file in the playbooks folder and include the following data

- docker_hub_password

## Deploy Playbook From CLI

Run the following command from the folder containing the playbooks:

```
ansible-playbook - [SERVER-IP/NAME-HERE], [PLAYBOOK-NAME].yml -e BUILD_VERSION=v1.6 -e BUILD_UPDATE=false -vvv
```

## Run Playbooks For 1st Build

- ansible-playbook -i my_droplet_ip, website.yml -e BUILD_VERSION=v1 -e BUILD_UPDATE=false -vvv

## Run Playbooks For Update

This will stop the current container and pull a new version and deploy as new container.

- ansible-playbook -i my_droplet_ip, website.yml -e BUILD_VERSION=v1 -e BUILD_UPDATE=true -vvv

