Acces_configuration
=========

Эта роль подготавливает сервер для использования.
1. Настраивает доступ по ssh по ключу.
2. Настраивает iptables.
3. Настраивает fail2ban.

Example Playbook
----------------

- hosts: all
  become: yes
  roles:
    - role: access
      tags: access

      ssh_port: 220

      configure_ssh: true
      configure_firewall: true
      configure_fail2ban: true


Author Information
------------------

Yuriy K.
