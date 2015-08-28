[![Build Status](https://travis-ci.org/RealSalmon/fogbutter.jenkins-master.svg?branch=master)](https://travis-ci.org/RealSalmon/fogbutter.jenkins-master)

fogbutter.jenkins-master
========================
A simple Jenkins install with options for using an nginx proxy and restoring
from a backup file

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
- jenkins_master_nginx_enforce_ssl_xfp: true
- jenkins_master_nginx_log_dir: "/var/log/nginx"
- jenkins_master_nginx_unlink_default: true

See defaults/main.yml for a description of role variables.

Dependencies
------------
None

Example Playbook
----------------
    ---
    - hosts: all
      roles:
        - jenkins-master

License
-------
BSD

Author Information
------------------
Ben Jones <ben@fogbutter.com>
