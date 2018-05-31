# Ansible playbooks for personal devices

This repository contains [Ansible](https://www.ansible.com/) playbooks to set up my devices, e.g. laptops or servers. Currently, only [Arch Linux](https://www.archlinux.org/) is supported.

```bash
ansible-playbook site.yml
```

## Playbooks

### site.yml

The `site.yml` playbook is for any device and uses the `common` role.

### desktop.yml

The `desktop.yml` playbook is for desktop devices, e.g. laptops. It uses the `common` and `gnome` roles.

## Roles

### common

The `common` role handles standard system tasks:

- Updates all packages
- (Arch Linux) Enables AUR and adds [Aurman](https://github.com/polygamma/aurman)
- Adds [Zsh](http://www.zsh.org/) and [Oh-My-ZSH](http://ohmyz.sh/)

### gnome

- Installs and configures [GNOME](https://www.gnome.org/)
- Adds [GNOME extensions](https://extensions.gnome.org/)
