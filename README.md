loewenstark/magento-22-php72
=====================

added some patches for Magento 2.2 to fix Issues with PHP 7.2

Requirements
------------
- PHP = 7.2.x
- Magento >= 2.2.7

Installation Instructions
-------------------------

```shell
~# composer require loewenstark/magento-22-php72
```

Modify your composer.json with the lines.
```
{
    "extra": {
        "enable-patching": true,
        "composer-exit-on-patch-failure": false,
        "patches-file": "composer.php72.json"
    }
}
```

you should also add the deployed "composer.php72.json" to your git Project Repository.
Modify your .gitignore with "!/composer.php72.json" to add this file to your Project.

To Fix "each function" in "colinmollenhour/cache-backend-file"
you have to install an other version

```
~# composer require colinmollenhour/cache-backend-file "v1.4.4 as v1.4"
```

To Avoid Issues with wrong PHP Version and missing MCrypt you can add this also to your composer.json

```
{
    "config": {
        "platform": {
            "php": "7.1.0",
            "ext-mcrypt": "1.0.0"
        }
    }
}
```

Support
-------
If you have any issues with this extension, open an issue on [GitHub](https://github.com/mklooss/magento2.2-php7.2/issues).

Contribution
------------
Any contribution is highly appreciated. The best way to contribute code is to open a [pull request on GitHub](https://help.github.com/articles/using-pull-requests).

Developer
---------
Mathis Klooß
[http://www.mage-profis.de/](http://www.mage-profis.de/)
[@gunah_eu](https://twitter.com/gunah_eu)

Licence
-------
[OSL - Open Software Licence 3.0](http://opensource.org/licenses/osl-3.0.php)

Copyright
---------
(c) 2019 Mathis Klooss