# RoHAWKticsScoutingAnsibleRPISetup

## Setup
```
sudo apt-get install ansible
add "localhost ansible_connection=local" to /etc/ansible/hosts
sudo apt-get install git
git clone https://github.com/HVA-FRC-3824/RoHAWKticsScoutingAnsibleRPISetup.git
cd RoHAWKticsScoutingAnsibleRPISetup
sudo ansible-playbook playbook.yml
```
## Add User
Modify users/tasks/main.yml by adding 
```
- name: <new user>
  user: name=<new user> password=$1$SomeSalt$33bf.WRvNM0IPNqSZE/iD0 groups=sudo
```
## Add apt-get install
Modify base_setup/tasks/main.yml by adding the new package to the with_items list (if you look in the file this makes sense)
