# Wordpress v0.1-bare

### About
Creates a new instance of wordpress, which can be installed using the Wordpress web installer.

### HowTo

#### Setup
Visit `mapped port 80` with a webbrowser to finish the installation.

#### Usage
Wordpress is fully managed via `mapped port 80`.

#### Maintenance
Backups can be performed via commandline:

```
docker exec <<<CONTAINER>>> /usr/bin/mysqldump -u root --password=example --all-databases > backup.sql
```

and restored via commandline:

```
cat backup.sql | docker exec -i <<<CONTAINER>>> /usr/bin/mysql -u root --password=example
```

### Credentials
-   MySQL root password: `example`
