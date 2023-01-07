# Git

## Install git

```bash
sudo apt install git
```

## Setup ssh key

```bash
ssh-keygen -t ed25519 -C "yosmanyga@gmail.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

# Ansible

```bash
sudo apt update

sudo apt install software-properties-common
sudo add-apt-repository --yes --update ppa:ansible/ansible
sudo apt install ansible

ansible-playbook --ask-become-pass init.yml
```
