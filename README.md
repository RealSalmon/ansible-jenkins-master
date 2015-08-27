[![Build Status](https://travis-ci.org/RealSalmon/fogbutter.jenkins-master.svg?branch=master)](https://travis-ci.org/RealSalmon/fogbutter.jenkins-master)

fogbutter.jenkins-master
========================
A very simple Jenkins install

Requirements
------------
Ubuntu 14.04 (certainly may work with others)

Role Variables
--------------
- jenkins_master_apt_key_url: "https://jenkins-ci.org/debian/jenkins-ci.org.key"
- jenkins_master_apt_key_id: "D50582E6"
- jenkins_master_apt_repo: "deb http://pkg.jenkins-ci.org/debian binary/"
- jenkins_master_backup_file_copy: no
- jenkins_master_backup_destination: /var/lib
- jenkins_master_backup_file: false

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
