En Dell 13, no detecta el firmware para la wifi. Pero funciona con el que tiene por defecto.
No seleccionar ningún Desktop. Solo standard system utilities.

# Clonezilla
Boot with UEFI.
Después de la instalación. Hacer copia del disk con Clonezilla.
Hay un paso en el que se inserta el disco donde se guardará la imagen. Luego se presiona Ctrl+C para continuar.

# Change font size in terminal

setfont /usr/share/consolefonts/Lat15-TerminusBold32x16.psf.gz

# Sudo

apt install sudo
usermod -aG sudo yosmanyga

# Mount usb

lsblk
mkdir /mnt/usb
mount /dev/sda1 /mnt/usb

# Gnome

apt install gnome-session gnome-terminal gnome-control-center nautilus gdm3

# Ansible

apt install ansible
ansible-galaxy collection install community.general

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
