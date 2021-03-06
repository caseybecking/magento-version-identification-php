# Magento Version Identification PHP

[![Packagist](https://img.shields.io/packagist/v/steverobbins/magento-version-identification.svg?style=flat-square)](https://packagist.org/packages/steverobbins/magento-version-identification)
[![Code Quality](https://img.shields.io/scrutinizer/g/steverobbins/magento-version-identification-php.svg?style=flat-square)](https://scrutinizer-ci.com/g/steverobbins/magento-version-identification-php/?branch=master)
[![Build Status](https://img.shields.io/travis/steverobbins/magento-version-identification-php.svg?style=flat-square)](https://travis-ci.org/steverobbins/magento-version-identification-php)

This is a PHP port of [Magento Version Identification](https://github.com/gwillem/magento-version-identification)

---

See [`version.json`](https://github.com/steverobbins/magento-version-identification-php/blob/master/version.json).

---

# Installation

```
git clone https://github.com/steverobbins/magento-version-identification-php
cd magento-version-identification-php
mkdir release
curl -sS https://getcomposer.org/installer | php
php composer.phar install
```

## With Composer

```
"require": {
    "steverobbins/magento-version-identification": "dev-master"
}
```

# Usage

Download your desired version(s) of Magento and place them in the `release` folder.  They should be named `CE-1.0`, `CE-1.1.0`, `EE-1.14.1.0`, etc.

Run the `generate` command to create hashes of all\* the files and save them to the `md5` folder.

```
./bin/mvi generate
```

To update the `version.json` file with unique hashes, run the `unique` command.

```
./bin/mvi unique
```

To find the edition and version of a Magento installation, use the `check` command.

```
./bin/mvi check http://demo.magentocommerce.com/
```
