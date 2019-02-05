Ansible Role: Nginx SSL Redirect
=========

This Role installs Nginx Web Server on a PC and redirect all the calls from HTTP to HTTPS. The index home page is named base.cu 

Requirements
------------

It no need Requeriments.

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

    nginx_conf_path: /etc/nginx
    nginx_sites_available: /etc/nginx/sites-available
    __nginx_packages:
    	- nginx
  		

Example Playbook
----------------

    - hosts: localhost
      remote_user: root
      roles:
    	- ansible-nginx-ssl-redirect

License
-------

BSD

Author Information
------------------

This role was created in 2019 by Jibsan Joel Rosa Toirac.
