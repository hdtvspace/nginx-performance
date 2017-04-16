# nginx-performance

The path for fastcgi_cache, client_body_temp_path are using the fast tmpfs in RAM under /run. 

To create these directories on startup automatic:

/etc/tmpfiles.d/nginx.conf
d /run/nginx 0775 root root - -
d /run/nginx-tmp 0775 root root - -

Also /var/run is a link to /run in most distributions.
