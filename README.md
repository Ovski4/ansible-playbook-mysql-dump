Mysql dump
==========

This playbook will dump a mysql database in a folder and delete dumps older than 7 days if prune is set to yes.

Usage example
-------------

### With ansible

```bash
ansible-playbook /var/www/ansible/playbooks/mysql-dump/main.yml \
    -e "mysql_dumps_target_folder=/var/folder/mysql_dumps" \
    -e "prune=yes" \
    -e "db_user=root" \
    -e "db_password=toto" \
    -e "db_host=mysql" \
    -e "db_name=userhere" \
```

### Using the ansible docker image with the docker-compose configuration

Update the `docker-compose.yml` file according to your needs.

```
docker-compose run mysql-dump
```
