Nginx_config
=========
Роль устанавливает nginx, подготавливает самоподписанный сертификат и конфиги, необходимые для работы wordpress через ssl.  

Example Playbook
----------------
    - role: nginx
        servername: "myserver.com"
        is_selfsigned_cert: true
        nginx_letsencrypt_cert_renewal: true

Используемые параметры
---------------
        servername - название сервера
        is_selfsigned_cert - подписывать ли сервер самоподписанным сертификатом.
        nginx_letsencrypt_cert_renewal - включать ли автоматическое обновление сертификата.

Author Information
------------------

Yuriy K.