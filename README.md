NGINX
=========



Requirements
------------

Installing a web server for the Debian family

Role Variables
--------------
defaults/main.yaml
<pre>
nginx_remove_default: true                          # remove nginx default site
nginx_template_path: "{{ role_path }}/templates"    # path to nginx site-template
</pre>

vars/main.yaml
<pre>
nginx_system_user: "www-data"
nginx_sites_enabled_path: /etc/nginx/sites-enabled
nginx_sites_available_path: /etc/nginx/sites-available
nginx_default_vhost_path: "{{ nginx_sites_enabled_path }}/default"
</pre>

Example Playbook
----------------

    - hosts: web
      vars: 
        nginx_remove_default: true|false
      roles:
        - ansible-role-nginx

License
-------

BSD

Author Information
------------------

NewErr0r
