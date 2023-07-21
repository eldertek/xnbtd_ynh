<!--
N.B.: This README was automatically generated by https://github.com/YunoHost/apps/tree/master/tools/README-generator
It shall NOT be edited by hand.
-->

# xNBTD for YunoHost

*[Lire ce readme en français.](./README_fr.md)*

> *This package allows you to install xnbtd quickly and simply on a YunoHost server.
If you don't have YunoHost, please consult [the guide](https://yunohost.org/#/install) to learn how to install it.*

## Overview

[xNBTD](https://github.com/eldertek/xnbtd) is a management application for delivery business. It facilitates the management of routes and schedules.


**Shipped version:** 0.0.9~ynh1
## Disclaimers / important information

## Links

* Report a bug about this package: https://github.com/eldertek/xnbtd/issues
* YunoHost website: https://yunohost.org/
* PyPi package: https://pypi.org/project/xnbtd/

These projects used `xnbtd`:

* https://github.com/eldertek/xnbtd

---

# Developer info

The App project will be stored under `__FINALPATH__` (e.g.: `/opt/yunohost/$app`) that's Django's `settings.FINALPATH`
"static" / "media" files to serve via nginx are under `__PUBLIC_PATH__` (e.g.: `/var/www/$app`) that's `settings.PUBLIC_PATH`

## package installation / debugging

This app is not in YunoHost app catalog. Test install, e.g.:
```bash
~# git clone https://github.com/eldertek/xnbtd_ynh.git
~# yunohost app install xnbtd_ynh/ -f
```
To update:
```bash
~# cd xnbtd_ynh
~/xnbtd_ynh# git fetch && git reset --hard origin/testing
~/xnbtd_ynh# yunohost app upgrade xnbtd_ynh -u . -F
```

To remove call e.g.:
```bash
sudo yunohost app remove xnbtd_ynh
```

Backup / remove / restore cycle, e.g.:
```bash
yunohost backup create --apps xnbtd_ynh
yunohost backup list
archives:
  - xnbtd_ynh-pre-upgrade1
  - 20201223-163434
yunohost app remove xnbtd_ynh
yunohost backup restore 20201223-163434 --apps xnbtd_ynh
```

Debug the installation, e.g.:
```bash
root@yunohost:~# cat /etc/yunohost/apps/xnbtd_ynh/settings.yml
...

root@yunohost:~# ls -la /var/www/xnbtd_ynh/
total 18
drwxr-xr-x 4 root root 4 Dec  8 08:36 .
drwxr-xr-x 6 root root 6 Dec  8 08:36 ..
drwxr-xr-x 2 root root 2 Dec  8 08:36 media
drwxr-xr-x 7 root root 8 Dec  8 08:40 static

root@yunohost:~# ls -la /opt/yunohost/xnbtd_ynh/
total 58
drwxr-xr-x 5 xnbtd_ynh xnbtd_ynh   11 Dec  8 08:39 .
drwxr-xr-x 3 root        root           3 Dec  8 08:36 ..
-rw-r--r-- 1 xnbtd_ynh xnbtd_ynh  460 Dec  8 08:39 gunicorn.conf.py
-rw-r--r-- 1 xnbtd_ynh xnbtd_ynh    0 Dec  8 08:39 local_settings.py
-rwxr-xr-x 1 xnbtd_ynh xnbtd_ynh  274 Dec  8 08:39 manage.py
-rw-r--r-- 1 xnbtd_ynh xnbtd_ynh  171 Dec  8 08:39 secret.txt
drwxr-xr-x 6 xnbtd_ynh xnbtd_ynh    6 Dec  8 08:37 venv
-rw-r--r-- 1 xnbtd_ynh xnbtd_ynh  115 Dec  8 08:39 wsgi.py
-rw-r--r-- 1 xnbtd_ynh xnbtd_ynh 4737 Dec  8 08:39 xnbtd_ynh_demo_settings.py

root@yunohost:~# cd /opt/yunohost/xnbtd_ynh/
root@yunohost:/opt/yunohost/xnbtd_ynh# source venv/bin/activate
(venv) root@yunohost:/opt/yunohost/xnbtd_ynh# ./manage.py check
xnbtd_ynh v0.8.2 (Django v2.2.17)
DJANGO_SETTINGS_MODULE='xnbtd_ynh_demo_settings'
PROJECT_PATH:/opt/yunohost/xnbtd_ynh/venv/lib/python3.7/site-packages
BASE_PATH:/opt/yunohost/xnbtd_ynh
System check identified no issues (0 silenced).

root@yunohost:~# tail -f /var/log/xnbtd_ynh/xnbtd_ynh.log
root@yunohost:~# cat /etc/systemd/system/systemd.service
...

root@yunohost:~# systemctl reload-or-restart xnbtd_ynh
root@yunohost:~# journalctl --unit=xnbtd_ynh --follow
```

## Documentation and resources

* Upstream app code repository: <https://github.com/eldertek/xnbtd>
* YunoHost documentation for this app: <https://yunohost.org/app_xnbtd>
* Report a bug: <https://github.com/YunoHost-Apps/xnbtd_ynh/issues>

## Developer info

Please send your pull request to the [testing branch](https://github.com/YunoHost-Apps/xnbtd_ynh/tree/testing).

To try the testing branch, please proceed like that.

``` bash
sudo yunohost app install https://github.com/YunoHost-Apps/xnbtd_ynh/tree/testing --debug
or
sudo yunohost app upgrade xnbtd -u https://github.com/YunoHost-Apps/xnbtd_ynh/tree/testing --debug
```

**More info regarding app packaging:** <https://yunohost.org/packaging_apps>
