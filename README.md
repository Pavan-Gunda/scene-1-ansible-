# Ansible Wireguard

A simple ansible playbook to install and Configure Wireguard Kubernetes Cluster 


## Requirements

 - Ansible 2.4 (or newer) installed on the machine that will run Ansible commands.

## Install
You must configure the inventory file in inventory/hosts.ini
 

    git clone https://github.com/ph4n666/ansible-.git
    cd ansible-
    # Edit inventory/hosts.ini
    ansible-playbook -i inventory/hosts.ini wireguard.yml

## Verify the installation
You can get the status of Wireguard by running the following command on every hosts

    wg show
 or with ansible

    ansible -i inventory/hosts.ini -a "wg show" wireguard

verify the Cluster state using 
```bash
Kubectl get pods
```
