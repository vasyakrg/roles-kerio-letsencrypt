### Роль nginx_deploy - для kerio-connect (debian 9)
- по списку доменов, создает для nginx конфиги, регистрирует через Letsencrypt сертификаты и подсовывает их в kerio-connect

#### Переназначаемые переменные:
```
nginx_deploy_listen_http: 80
nginx_deploy_listen_https: 443

nginx_deploy_vhost_template: "vhost.j2"
nginx_deploy_vhost_path: "/etc/nginx/sites-enabled"
nginx_deploy_logs_path: "/var/log/nginx"
nginx_deploy_root_group: "www-data"
nginx_deploy_certpath: "/opt/kerio/mailserver/sslcert"
nginx_deploy_letsencrypt_email: test@mail.ru

nginx_deploy_vhosts:
  - server_name: test.local
    file_name: test.local.conf
    state: present
    index: present
```

##### Автор
- **Vassiliy Yegorov** - *Initial work* - [vasyakrg](https://github.com/vasyakrg)
- [сайт](vk.com/realmanual)
- [youtube](youtube.com/realmanual)
