# ansible-beats-linux

**THIS ROLE IS UNDER ACTIVE DEVELOPMENT AND IS NOT SUITABLE FOR USAGE IN PRODUCTION!!! .**

**THIS ROLE IS FOR 6.x**

Ansible role for 6.x/5.x filebeat.  Currently this works on Debian and RedHat based linux systems.  Tested platforms are:

* Debian 9


test
Metricbeat configuration values:
```
mb_version_lock: false
mb_upgrade: false
mb_version: "6.4.1"
mb_name: "as19376105871-1604810"
mb_fields:
hc_src_ip: "{{ ansible_default_ipv4.address }}"
mb_modules:
  - "system"
  - "apache"
  - "docker"
  - "mysql"
  - "nginx"
mb_system_period: 10s
mb_nginx_host: http://127.0.0.1
mb_nginx_period: 10s
mb_nginx_server_status: server-status
mb_mysql_period: 10s
mb_mysql_host: root:secret@tcp(127.0.0.1:3306)/
mb_mysql_username: root
mb_mysql_password: secret-hostsfile
mb_apache_period: 10s
mb_apache_host: http://127.0.0.1
mb_apache_server_status: server-status
mb_apache_username: root
mb_apache_password: secret
mb_docker_host: unix:///var/run/docker.sock
mb_docker_period: 10s
```