# Ansible playbooks for personal devices

This repository contains [Ansible](https://www.ansible.com/) playbooks to set up my devices, e.g. laptops or servers. Currently, only [Arch Linux](https://www.archlinux.org/) is supported.

```bash
ansible-playbook site.yml
```

The `site.yml` playbook

- Updates all packages
- (Arch Linux) Enables AUR and adds [Aurman](https://github.com/polygamma/aurman)
- Adds [Zsh](http://www.zsh.org/) and [Oh-My-ZSH](http://ohmyz.sh/)
