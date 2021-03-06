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

### developer.yml

The `developer.yml` playbook is for desktop devices on which I develop, e.g. laptops. It uses the `common`, `gnome` and all `*-developer` roles.

Individual `<flavour>-developer` roles can be excluded by skipping the `<flavour>` tag:

```bash
ansible-playbook developer.yml --skip-tags <flavour>

# Skip the java-developer role
ansible-playbook developer.yml --skip-tags java
```

## Roles

### common

The `common` role handles standard system tasks:

- Standard system configuration, e.g. localization
- Adds [Git](https://git-scm.com/), [Zsh](http://www.zsh.org/) and [oh-my-zsh](http://ohmyz.sh/)
- Includes the `common-archlinux` role on Arch Linux distributions

### common-archlinux

- Configures [Systemd-boot](https://wiki.archlinux.org/index.php/Systemd-boot)
- Enables AUR and adds [Aurman](https://github.com/polygamma/aurman)
- Updates all packages, including AUR

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
