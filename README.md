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


**Shipped version:** 2.0.2~ynh1
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

## Documentation and resources

* Upstream app code repository: <https://github.com/eldertek/xnbtd>
* YunoHost documentation for this app: <https://yunohost.org/app_xnbtd>
* Report a bug: <https://github.com/eldertek/xnbtd_ynh/issues>

## Developer info

Please send your pull request to the [testing branch](https://github.com/eldertek/xnbtd_ynh/tree/testing).

To try the testing branch, please proceed like that.

``` bash
sudo yunohost app install https://github.com/eldertek/xnbtd_ynh/tree/testing --debug
or
sudo yunohost app upgrade xnbtd -u https://github.com/eldertek/xnbtd_ynh/tree/testing --debug
```

**More info regarding app packaging:** <https://yunohost.org/packaging_apps>
