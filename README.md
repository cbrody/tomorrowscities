## Code for [Tomorrows Cities](https://tomorrowscities.org) website

//[![Build Status](https://travis-ci.org/cbrody/tomorrowscities.svg)](https://travis-ci.org/cbrody/tomorrowscities)

## Installation

You will need a local development environment providing a webserver, php >= 7.3 and mySQL / mariaDB. [Full requirements](https://www.drupal.org/docs/system-requirements)

Clone this repository and check out the [latest release](https://github.com/cbrody/tomorrowscities/releases/latest) to `some-dir`.

[Install composer](https://getcomposer.org/doc/00-intro.md#installation-linux-unix-osx) if not already installed

> Note: The instructions below refer to the [global composer installation](https://getcomposer.org/doc/00-intro.md#globally).
You might need to replace `composer` with `php composer.phar` (or similar)
for your setup.

Install the project:

```
cd some-dir
composer install
```

Create an empty database (mySQL/mariaDB is preferred) and an associated user with full rights to the schema.

Copy `web/sites/default/default.settings.php` to `settings.php`

Install Drupal, using default settings and the database/user credentials as created.

Overwrite the database with the latest version from production, e.g. `drush sqlc < /path/to/tc.sql`

Copy site files e.g. `rsync -zarvh /path/to/source/files/* web/sites/default/files`

`drush cr` To rebuild the caches
