# Ansible Role: Apache PHP-FPM
Configures Apache for PHP-FPM usage.

## Requirements
This role requires that you have PHP-FPM installed on the server.

## Role Variables
None.

## Dependencies
This role has a dependency for `damianlewis.apache`.

## Example Playbook
```yaml
- hosts: server
  become: yes

  vars:
    apache_sites:
    - hostname: example.test
      root: /var/www/html

  tasks:
  - import_role:
      name: damianlewis.apache-php-fpm
```
