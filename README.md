# Halcyon for Mastodon
A Mastodon web client

<img src="https://halcyon.social/login/assets/images/preview0.png"/>

## Demo
https://halcyon.social/

## Features
- Twitter like UI, familiar interface.
- Able to use on all instances.
- No tracking, No ads.

## Requirement
- Apache
- PHP
- MySQL

## Setup(仮)
I didn't prepared setup script so you have to setup manually...

### PDO MySQL

After installed PHP, run this.

```bash
sudo pecl install pdo_mysql
sudo vi php.ini
```

change to this

```php.ini
extension=mysqli.so
extension=pdo_mysql.so
```

### MySQL
After installed MySQL, create a user, run this.
```sql
CREATE DATABASE DATABASE_NAME DEFAULT CHARACTER SET utf8;
CREATE TABLE DATABASE_NAME.instances(domain varchar(261), client_id varchar(64), client_secret varchar(64));
```
and make file `/config.ini` like this
```config.ini
~~~ line 3 ~~~
api_client_name = <APP NAME>
api_client_website = <APP WEBSITE LINK>
~~~ line 8 ~~~
db_host = <DATABASE HOST DOMAIN>
db_user = <DATABASE USERNAME>
db_pass = <DATABASE PASSWORD>
db_name = <DATABASE NAME>
```

## Credits

- [Kirschn/mastodon.js](https://github.com/Kirschn/mastodon.js)
- [yks118/Mastodon-api-php](https://github.com/yks118/Mastodon-api-php)
