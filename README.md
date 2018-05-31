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

### java-developer

- Installs [OpenJDK 10](http://openjdk.java.net/), [Groovy](http://groovy-lang.org/) and [Kotlin](https://kotlinlang.org/)
- Adds [Maven](https://maven.apache.org/) and [Gradle](https://gradle.org/)
- Adds [Docker](https://www.docker.com/) and [Docker Compose](https://docs.docker.com/compose/)
- Adds [IntelliJ IDEA Ultimate](https://www.jetbrains.com/idea/) and [Visual Studio Code](https://code.visualstudio.com/)

### python-developer

- Installs [Python](https://www.python.org/) and [pip](https://pypi.org/project/pip/)
- Adds [Docker](https://www.docker.com/) and [Docker Compose](https://docs.docker.com/compose/)
- Adds [IntelliJ IDEA Ultimate](https://www.jetbrains.com/idea/) and [Visual Studio Code](https://code.visualstudio.com/)
