Role Name
=========

Installation of a containerised Wordpess environment

Requirements
------------

Linux Ubunutu or Centos distribution required
ssh key acces 
root acces 

Role Variables
--------------
    ctnMysql: Container's mariaDb name
    ctnWordpress: Container's wordpress name
    ntwWordpress: Docker Network's name
    volDb: Docker database's name volume
    exposePort: Exposed port's  of wordpress


Dependencies
------------
Galaxie role
steissier.docker_role


Example Playbook
----------------
---
- hosts: all
  vars:
    ctnMysql: "mySql"
    ctnWordpress: "wordpress"
    ntwWordpress: "wordpress_network"
    volDb: "db"
    exposePort: "8080"
  become: true
  roles:
    - steissier.docker_role
    - role_wordpress
---


License
-------

Free

Author Information
------------------

Seb the aprentice
