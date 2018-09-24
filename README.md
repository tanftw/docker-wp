# Docker Setup For WordPress
Up And Running Full WordPress Server In Seconds

## What's inside?

- Latest WordPress (4.9.x)
- Latest PHP (7.2.x)
- Apache with `000-default.conf` vhost and the default domain is `wp.test`.
- MySQL 5.7
- PHPMyAdmin (default logged in).
- `.env` file for configuration.
- `.editorconfig` file for better code styling in whole WordPress project.

## How?
- Download and install Docker.
- Clone the project.
- Run `docker-compose up -d` in the same folder with `docker-compose.yml`.
- Add `127.0.0.1 wp.test` to your hosts file.

## Usage?

**Change Domain**

Edit domain in the `.docker/apache/000-default.conf`. Default is *wp.test*.

**Default MySQL Credentials**

You can check the `.env` file. Default credentials is:

```
DB_USER=root
DB_NAME=wp
DB_PASSWORD=root
DB_HOST=mysql:3306
```

**Access PHPMyAdmin**

Just go to *localhost:8080*. You don't need to enter either user name or password tho.

**Disable PHPMyAdmin Auto Login**

By default, you'll be logged in automatically, but in production server, you'll want to disable this. Just remove `PMA_USER` and `PMA_PASSWORD` row in `docker-compose.yml`

## Future?
- Allows user setup domain in `.env` file.
- Blackfire.io support
- XDebug support
