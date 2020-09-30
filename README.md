# climb-workshop-ansible
Based on https://github.com/PoreCamp/porecamp.github.io/tree/master/ansible-recipes


Install ansible
```
sudo apt-get update
sudo apt-get install software-properties-common
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update
sudo apt-get install ansible
```

Generate ssh key
```
ssh-keygen
cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys
```
and add the following to `/etc/ansible/hosts`
```
[localhost]
127.0.0.1
```
test with `ssh localhost` then `exit`

Install git and clone this repo
```
sudo apt-get install git
git clone https://github.com/annacprice/climb-workshop-ansible.git
```

Run `generate_user_passwords.py` to generate `users.yml`

Run `prepare_vm.yml`
```
ansible-playbook -s prepare_vm.yml
```
