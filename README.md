# climb-workshop-ansible
Based on https://github.com/PoreCamp/porecamp.github.io/tree/master/ansible-recipes


Install python3 and ansible
```
sudo apt-get update
sudo apt-get install -y python3 python3-pip
sudo pip3 install ansible 
```

Generate ssh key
```
ssh-keygen
cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys
```
and add the following to `/etc/ansible/hosts`
```
[localhost]
127.0.0.1 ansible_python_interpreter=/usr/bin/python3
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
ansible-playbook prepare_vm.yml
```
