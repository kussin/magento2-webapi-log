# Magento 2 WebAPI Logger (REST) modified by Kussin | eCommerce und Online-Marketing

**NOTE:** This module is a fork of the original [Magento 2 WebAPI Logger (REST)](https://github.com/vladflonta/magento2-webapi-log). It adds additional settings to the module configuration like enabling/disabling of scopes.

A Magento module for logging all REST API requests as text files in var/log/webapi_rest/ folder.

## Installation steps

### Get the module via composer

In order to install the module via composer, run the following commands in commandline of your shop base directory 
(where the shop's composer.json file resides).

```
composer require "vladflonta/magento2-webapi-log":"~0" --no-update
```

#### Add fork to composer.json

Read for more details: https://stackoverflow.com/a/13500676

```
{
    "repositories": [
        "kussin_oxidcaotchamodule": {
            "type": "vcs",
            "url": "https://github.com/kussin/oxid-captcha-module.git"
        }
    ],
    "require": {
        "oxid-projects/captcha-module": "dev-master"
    }
}
```

And then run the following command in commandline of your shop base directory (where the shop's composer.json file resides).

```
composer update --no-interactions
```

### Module installation via repository cloning

```
git clone https://github.com/kussin/magento2-webapi-log.git app/code/VladFlonta/WebApiLog
```

### Enable module

```
bin/magento module:enable VladFlonta_WebApiLog
bin/magento setup:upgrade
```

## Usage

The modules logs requests to subfolders in the `var/log/webapi_rest` according to the REST route.

Example: `var/log/webapi_rest/integration/admin/token/20181213_082324.log`

Remark: Auth requests do not contain body / response to avoid a security breach.

## User Guide

[User Guide](USER_GUIDE.md)

## Support

Kussin | eCommerce und Online-Marketing GmbH<br>
Fahltskamp 3<br>
25462 Rellingen<br>
Germany

Fon: +49 (4101) 85868 - 0<br>
Email: info@kussin.de

## License

This project is licensed under the [Open Software License (OSL 3.0)](http://opensource.org/licenses/osl-3.0.php)

## Copyright

(c) 2006-2022 Kussin | eCommerce und Online-Marketing GmbH
