# Introduction
This guide assumes that you're familiar with setting up [Laravel application](https://laravel.com/docs/7.x/).

If you don't have a working web-server & want to create a new one, You can follow this concise article by [Digital Ocean](https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-18-04)

## Setting up the project
First step is cloning the project in the repository of your choice. Next is as follow.

1. copy .env.example to .env
2. Run `composer install`
3. Set your database environment details in .env file.
4. Run `php artisan migrate` 
   (Optionally add `--seed` if you don't have database-dump.sql)

5. Set `SCOUT_DRIVER` to `[tntsearch](https://github.com/teamtnt/laravel-scout-tntsearch-driver#installation)`
   > In `config/scout.php` you will find array called `tntsearch` it is responsible for creating indexes for search in our application. You want to make sure that user www-data has proper write permission to storage_path.
   
### Backend Server NGINX configuration

Adding this line is very important for CORS image access to front-end `add_header 'Access-Control-Allow-Origin' '*';`

```
server {
    listen 80;
    listen 443 ssl http2;
    server_name .parasdham.local;
    root "/home/vagrant/parasdham/public";

    index index.html index.htm index.php;

    charset utf-8;        

    location / {
        try_files $uri $uri/ /index.php?$query_string;        
        add_header 'Access-Control-Allow-Origin' '*';
    }

    location = /favicon.ico { access_log off; log_not_found off; }
    location = /robots.txt  { access_log off; log_not_found off; }

    access_log off;
    error_log  /var/log/nginx/parasdham.local-error.log error;

    sendfile off;

    location ~ \.php$ {
        fastcgi_split_path_info ^(.+\.php)(/.+)$;
        fastcgi_pass unix:/var/run/php/php7.4-fpm.sock;
        fastcgi_index index.php;
        include fastcgi_params;
        fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
        

        fastcgi_intercept_errors off;
        fastcgi_buffer_size 16k;
        fastcgi_buffers 4 16k;
        fastcgi_connect_timeout 300;
        fastcgi_send_timeout 300;
        fastcgi_read_timeout 300;
    }

    location ~ /\.ht {
        deny all;
    }

    ssl_certificate     /etc/nginx/ssl/parasdham.local.crt;
    ssl_certificate_key /etc/nginx/ssl/parasdham.local.key;
}
```
