[![Build Status](https://travis-ci.org/RealSalmon/ansible-jenkins-master.svg?branch=master)](https://travis-ci.org/RealSalmon/ansible-jenkins-master)

RealSalmon.jenkins-master
=========================
A simple Jenkins install with options for using an nginx proxy and restoring
from a backup file

https://galaxy.ansible.com/list#/roles/4900

Requirements
------------
- Ubuntu 14.04
- Ansible 1.9

Role Variables
--------------
- jenkins_master_apt_key_url: "https://jenkins-ci.org/debian/jenkins-ci.org.key"
- jenkins_master_apt_key_id: "D50582E6"
- jenkins_master_apt_repo: "deb http://pkg.jenkins-ci.org/debian binary/"
- jenkins_master_backup_file_copy: false
- jenkins_master_backup_destination: "/var/lib"
- jenkins_master_backup_file: false
- jenkins_master_nginx_proxy: false
- jenkins_master_nginx_server_name: "_"
- jenkins_master_nginx_enforce_ssl_xfp: false
- jenkins_master_nginx_enforce_ssl: false
- jenkins_master_nginx_log_dir: "/var/log/nginx"
- jenkins_master_nginx_unlink_default: true
- jenkins_master_nginx_ssl: false
- jenkins_master_nginx_ssl_protocols: "TLSv1 TLSv1.1 TLSv1.2"
- jenkins_master_nginx_ssl_crt: "/etc/nginx/ssl/{{ jenkins_master_nginx_server_name }}.crt"
- jenkins_master_nginx_ssl_key: "/etc/nginx/ssl/{{ jenkins_master_nginx_server_name }}.key"
- jenkins_master_nginx_ssl_s3_bucket: false
- jenkins_master_nginx_ssl_s3_crt: "jenkins-master.crt"
- jenkins_master_nginx_ssl_s3_key: "jenkins-master.key"
- jenkins_master_nginx_ssl_s3_access_key: ""
- jenkins_master_nginx_ssl_s3_secret_key: ""
- jenkins_master_nginx_ssl_s3_region: "us-east-1"
- jenkins_master_nginx_ssl_awscli_source: "pip"

See defaults/main.yml for a description of role variables.

Dependencies
------------
None

Example Playbook
----------------
    ---
    - hosts: all
      roles:
        - RealSalmon.jenkins-master

License
-------
BSD

Author Information
------------------
Ben Jones <ben@fogbutter.com>
