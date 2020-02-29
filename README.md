nginx
=====


What is does this role do?
--------------------------

This role installs and configures the nginx webserver for drop in
operation of other roles.  This role provides the 'nginx' handler and
is depended on by many other web roles.


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
  * nginx_dhparam_bits: 2048
  * nginx_bind_443: false
  * use_ssl: false
  * ssl_resolvers_v4:
    - "8.8.8.8"
  * ssl_resolvers_v6:
    - "2001:4860:4860::8888"
  * ssl_session_timeout: 1d
  * ssl_session_cache: "shared:SSL:50m"
  * ssl_protocols: TLSv1.2
  * ssl_dhparam: /etc/nginx/dhparam.pem
  * ssl_stapling: no
  * ssl_ciphers:
    - ECDHE-ECDSA-AES256-GCM-SHA384
    - ECDHE-RSA-AES256-GCM-SHA384
    - ECDHE-ECDSA-CHACHA20-POLY1305
    - ECDHE-RSA-CHACHA20-POLY1305
    - ECDHE-ECDSA-AES128-GCM-SHA256
    - ECDHE-RSA-AES128-GCM-SHA256
    - ECDHE-ECDSA-AES256-SHA384
    - ECDHE-RSA-AES256-SHA384
    - ECDHE-ECDSA-AES128-SHA256
    - ECDHE-RSA-AES128-SHA256

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
