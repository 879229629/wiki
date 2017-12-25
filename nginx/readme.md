## 依赖软件

```
yum install gcc && yum install yum install gcc-c++
```

## 依赖包

https://www.nginx.com/resources/admin-guide/installing-nginx-open-source/#dependencies


## openssl install

https://www.ehowstuff.com/how-to-install-and-update-openssl-on-centos-6-centos-7/

## 

```

./configure
--sbin-path=/usr/local/nginx/nginx
--conf-path=/usr/local/nginx/nginx.conf
--pid-path=/usr/local/nginx/nginx.pid
--with-pcre=../pcre-8.41
--with-zlib=../zlib-1.2.11
--with-http_ssl_module
--with-stream
--with-mail=dynamic
--add-module=/usr/build/nginx-rtmp-module
--add-dynamic-module=/usr/build/3party_module

```

## config 

https://gist.github.com/plentz/6737338

## https config
https://keelii.github.io/2016/06/12/free-https-cert-lets-encrypt-apply-install/
http://seanlook.com/2015/05/28/nginx-ssl/

```

./certbot-auto certonly --webroot --agree-tos -v -t --email 邮箱地址 -w 网站根目录 -d 网站域名
./certbot-auto certonly --webroot --agree-tos -v -t --email zenggang.king@gmail.com -w /data/app/ -d 879229629.com

        listen       443 ssl;
        server_name  879229629.com;


        ssl on;
        ssl_certificate /etc/letsencrypt/live/879229629.com/fullchain.pem;
        ssl_certificate_key /etc/letsencrypt/live/879229629.com/privkey.pem;
        ssl_trusted_certificate /etc/letsencrypt/live/879229629.com/chain.pem;
        ssl_dhparam /usr/local/nginx/ssl/dhparams.pem;
        ssl_protocols TLSv1 TLSv1.1 TLSv1.2;
        ssl_ciphers HIGH:!aNULL:!MD5;

        ssl_session_cache    shared:SSL:1m;
        ssl_session_timeout  5m;
        ssl_prefer_server_ciphers  on;

```




