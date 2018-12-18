# Ansible Role: Apache PHP-FPM
Configures Apache for PHP-FPM usage.

## Requirements
This role requires that you have PHP-FPM installed on the server.

## Role Variables
Available variables are listed below, see `defaults/main.yml` for the default values.

```yaml
apache_php_fpm_conf_files:
- php7.1-fpm
- php7.2-fpm
```
By default, version 7.0 of PHP-FPM is enabled. You can change which versions to enable by adding them to the `apache_php_fpm_conf_files` variable.

## Dependencies
This role has a dependency for `damianlewis.apache`.

## Example Playbook
```yaml
- hosts: server
  become: yes

  vars:
    apache_sites:
    - hostname: www.example.com
      root: /var/www/html

  tasks:
  - import_role:
      name: damianlewis.apache
  - import_role:
      name: damianlewis.apache-php-fpm
```
