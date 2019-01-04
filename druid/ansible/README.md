# Druid installation playbook
##Requirements
* Centos =< 7

##Directory overview
This direcotry contain the following files:
* `playbook.yml`
* `inventory.ini`

### Inventory description
The inventory file describes which vm should be used in the following playbook:  
```ini
[druid-vm]

[druid-vm:vars]
ansible_user=
ansible_ssh_private_key_file=
```
**ansible_user** - user that should be used in order to connect the vm (root)  
**ansible_ssh_private_key_file** - private key location in order to connect the vm, the public key should be in the vm.   

### Playbook description
The playbook contain the roles that should apply on the specified hosts:  

```yamlex
  name: Installing Druid vm
  hosts: druid-vm
  roles:
    - druid
```
**name** - name of the play  
**hosts** - the hosts specified in the inventory file.  
**roles** - roles that should involve the ansible run.

## How to deploy
1. Install ansible.
2. Run the follow command from the current directory:  
 ``ansible-playbook -i inventory.ini playbook.yml``