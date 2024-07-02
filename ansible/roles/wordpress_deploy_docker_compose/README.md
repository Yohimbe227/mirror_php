Role Name
=========

Эта роль подготавливает к разворачиванию через docker compose Wordpress и разворачивает ее.

Requirements
------------

Для корректной работы роли необходимо установить модуль из коллекции community.docker:

ansible-galaxy collection install community.docker

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: wordpress

Нет дополнительный параметров.

Author Information
------------------

Yuriy K.
