Ansible Role: Nginx SSL Redirect
=========

This Role installs Nginx Web Server on a PC and redirect all requests from HTTP to HTTPS. The index home page is named base.cu
If you want to delete this, you should go into:

    ansible-nginx-ssl-redirect/files/default

and delete the following line in the entire document

    server_name base.cu;


Requirements
------------

It needs no extra roles. You must eddit your resolv.conf and add a line like this:

    192.168.14.999 base.cu

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
