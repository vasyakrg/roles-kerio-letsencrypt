### Роль автоматизированной установки SSL сертификатов для kerio-connect 9.х (debian 9)
- по списку доменов, регистрирует через Letsencrypt сертификаты и подсовывает их в kerio-connect

#### Переназначаемые переменные:
```
lets_deploy_certpath: "/opt/kerio/mailserver/sslcert"
lets_deploy_letsencrypt_email: test@mail.ru

lets_deploy_vhosts:
  - server_name: test.local
    state: present # or **absent**

lets_monthly: "monthly" # crontab time job
lets_crontab_enable: "enable" # crontab enable to add job, or "disable" to delete job

lets_dry_run: "--dry-run" # dry_run execute certbot or "" to run actual job
```

##### Автор
- **Vassiliy Yegorov** - *Initial work* - [vasyakrg](https://github.com/vasyakrg)
- [сайт](vk.com/realmanual)
- [youtube](youtube.com/realmanual)
