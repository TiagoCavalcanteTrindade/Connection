# Connection
A PHP library that do SQL querys

## Getting started
First, check if you meet all of the **prerequisites**, after it **install**
### Prerequisites
#### MySQL prerequisites
1. Install the MySQL and configure it
2. In the file `php.ini` (if it doesn't exists rename the file `php.ini-development` to `php.ini`) remove the `;` before the `extension=mysqli` (it's probably in the line 922)
#### SQLite prerequisites
1. In the file `php.ini` (if it doesn't exists rename the file `php.ini-development` to `php.ini`) remove the `;` before the `extension=sqlite3` (it's probably in the line 942)
### Instalation
To install you need to execute the command bellow:
```bash
git submodule add https://github.com/TiagoCavalcanteTrindade/Connection
```

## Documentation
The Documentation link goes [here](https://github.com/TiagoCavalcanteTrindade/Connection/wiki)

## Tests
### Before init
Before init you need to execute the command bellow:
```bash
composer install
```
Before init you need to create the files `MySQL.env.php` and `SQLite.env.php` in the folder `tests`.
The file `MySQL.env.php` need to have the `env`s `host`, `user`, `password` and `database`, e.g.:
```php
<?php
	putenv('host=localhost');
	putenv('user=root');
	putenv('password=');
	putenv('database=database');
?>
```
The file `SQLite.env.php` need to have the `env` `database`, e.g.:
```php
<?php
	putenv('database=databases/database.sqlite3');
?>
```
### Execute the tests
* If you're on Linux execute the command bellow: (it's necessary execute this on the project root folder):
  ```bash
  ./vendor/bin/phpunit tests
  ```
* If you're on Windows execute the command bellow: (it's necessary execute this command on the project root folder):
  ```bash
  call vendor/bin/phpunit tests
  ```