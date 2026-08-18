ABOUT
=====

A radically simple Ansible role.
- System: Debian
- State: Probably Production

PLAYBOOK
========

```yml
# libreoffice
# Flatpak version requires cups-browsed for printing
- ansible.builtin.import_role:
	  name: libreoffice
  vars:
    libreoffice_user: Brigitte
    libreoffice_flatpak_overrides:
    Context:
      sockets: "!fallback-x11;!x11"
      filesystems: "/media/{{ libreoffice_user }}/nas/common;home;!host"
```