# Использование роли
    - role: nginx
        nginx_configs: files(или templates)/nginx
        nginx_letsencrypt_cert_renewal: true
        nginx_letsencrypt_cert:
            - domain1.com
        nginx_selfsigned_cert:
            - domain2.com
        nginx_vhosts:
            - XXX.students.devboxops.xyz
            - XXX.proxied.students.devboxops.xyz

## Используемые параметры
nginx_configs - путь по которому лежит шаблон конфига nginx.
nginx_letsencrypt_cert_renewal - обновлять или нет ssl сертификат.
nginx_letsencrypt_cert - на какой домен выпускать сертификат Letsencrypt.
nginx_selfsigned_cert - на какой домен выпускать самоподписанный сертификат.
nginx_vhosts - виртуальные хосты, которые нужно сконфигурировать.