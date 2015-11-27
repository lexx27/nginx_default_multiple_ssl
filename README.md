# nginx_default_multiple_ssl
The default nginx catchall for vhosts that dont have ssl

A self-signed ssl is required for this to work

```
server {
        listen 443 ssl default_server;
        listen [::]:443 default_server;


        return 503;
        server_name example.com;
        ssl on;
        ssl_certificate /etc/nginx/ssl/default_nginx.crt;
        ssl_certificate_key /etc/nginx/ssl/default_nginx.key;

}

```
