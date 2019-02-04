nginx
=====


What is does this role do?
--------------------------

This role installs and configures the nginx webserver for drop in operation of other roles.  This role provides the 'nginx' handler and is depended on by many other web roles.


Meta
----

Files Managed:
  * /etc/iptables.d/nginx.rules
  * /etc/nginx/nginx.conf
  * /srv/www/
  * /etc/nginx/sites-available
  * /etc/nginx/sites-enabled
  * /var/service/nginx

Defaults Provided:
  * None

Variables Required:
  * None

Optional Variables:
  * `nginx_acme_challenge_path`

Files Required:
  * None

Optional Files:
  * None

Conflicting Roles:
  * None

Depends On:
  * [network](https://github.com/void-ansible-roles/network)
