Role Name
=========

Role to install logstash 

Requirements
------------

- Modify vars/main.yml and specify your own settings. elasticsearch domain is required
- Replace  files/logstasj.crt and logstash.key with your own certificate and key
- This example will install a filter for apache access log. You will need to create your own filters and add them in files/10-lumberjack-filter.conf

 Role Variables
--------------
java: sun-java-1.8.0_25-1.x86_64 - can be replaced with other version
logstash: logstash-1.5.0.rc2-1.noarch - can be replaced with other version
logstash_ssl_dir: /etc/logstash/certs - location for the certificate and key
logstash_ssl_key_file: logstash.crt - certificate name
logstash_ssl_certificate_file: logstash.key - certificate key
logstash_elasticsearch_host: elasticsearch001.yourdomain - replace with your elasticsearch domain
logstash_elasticsearch_cluster: elasticsearch   - replace with the name of your elasticsearch cluster


Dependencies
------------


Example Playbook
----------------
- hosts: host-group
  sudo: yes
  roles:
    - role: logstash


License
-------

BSD

Author Information
------------------
devopsjournal.org
