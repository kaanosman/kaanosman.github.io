---
layout: post
categories: programs
title: LEMP Stack Kurulumu
excerpt: "Ubuntuya LEMP Stack kurulumu"
tags: [lemp, stack, linux, nginx, mysql , php]
comments: true
--- 

LEMP stack linux üzerinde [nginx](http://nginx.org/), [Mysql](https://www.mysql.com/) ve [Php](http://php.net/) kullanarak uygulama geliştirmeye yarayan programlar topluluğudur. Web sunucu olarak nginx kullanır. Nginx hızlı, yüksek performanslı, ücretsiz, düşük cpu ve ram kullanan bir web sunucu olduğu için alternatiflerine göre(apache, lighthttp, litespeed, zeus) kullanım oranı son yıllarda gittikçe artmaktadır. Mysql ise oldukça hızlı ve dökümantasyonu zengin bir veri tabanıdır. Php ise web uygulamaları oluşturmak için biçilmiş kaftandır diyebiliriz. Bütün bunları yazacağımız işletim sistemi tabi ki linux olamalı.

#### 1)Nginx Kurulumu

* sudo apt-get install nginx
* sudo service nginx start
* http://localhost

#### 2) Mysql Kurulumu

* sudo apt-get install mysql-server php5-mysql
* sudo mysql_install_db
* sudo /usr/bin/mysql_secure_installation

#### 3)Php Kurulumu

* sudo apt-get install php5-fpm fhp5-cli

#### 4)Php Ayarları

* sudo gedit /etc/php5/fpm/php.ini dosyasını açıp **CGİ.FİX_PATHİNFO=1** satırını bulup değeri 1 ise 0 yapmalıyız.
* sudo service restart php5-fpm

#### 5)Nginx Ayarları

* sudo gedit /etc/nginx/sites-available/default


server {

	listen 80 default_server;
	listen [::]:80 default_server ipv6only=on;

	root /usr/share/nginx/html;
	index index.php index.html index.htm;

	# Make site accessible from http://localhost/
	server_name localhost;

	location / {
		# First attempt to serve request as file, then
		# as directory, then fall back to displaying a 404.
		try_files $uri $uri/ =404;
		# Uncomment to enable naxsi on this location
		# include /etc/nginx/naxsi.rules
	}

	# Only for nginx-naxsi used with nginx-naxsi-ui : process denied requests
	#location /RequestDenied {
	#	proxy_pass http://127.0.0.1:8080;    
	#}

	error_page 404 /404.html;

	# redirect server error pages to the static page /50x.html
	#
	#error_page 500 502 503 504 /50x.html;
	location = /50x.html {
		root /usr/share/nginx/html;
	}

	# pass the PHP scripts to FastCGI server listening on 127.0.0.1:9000
	#
	location ~ \.php$ {
		fastcgi_split_path_info ^(.+\.php)(/.+)$;
	#	# NOTE: You should have "cgi.fix_pathinfo = 0;" in php.ini
	#
	#	# With php5-cgi alone:
	#	fastcgi_pass 127.0.0.1:9000;
	#	# With php5-fpm:
		fastcgi_pass unix:/var/run/php5-fpm.sock;
		fastcgi_index index.php;
                fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
		include fastcgi_params;
	}

	# deny access to .htaccess files, if Apache's document root
	# concurs with nginx's one
	#
	#location ~ /\.ht {
	#	deny all;
	#}
        }

* sudo service nginx restart

#### 6)Nginx Root Klasör Değiştirme(Tercihen)

Nginxin varsayılan root klasörü **/usr/share/nginx/html** klasörüdür. Yani browsera http://localhost yazdığımızda bu klasörün içindeki index.php çalışır. Root klasörünü izin vererek kullanabilirsiniz ama kendi oluşturduğunuz çalışma dizininizi root klasörü yapmanız daha kullanışlı olur. Bunun için ;

* sudo gedit /etc/nginx/sites-available/default

komutunu çalıştırıp açılan sayfada **root /usr/share/nginx/html;** yazan yeri çalışma dizininizin pathi ile değiştirmelisiniz. Örneğin home dizini altında php klasörü oluşturup onu root yapmak için **root /home/username/php;** şeklinde değiştirmelisiniz.

#### 7)Phpmyadmin Kurulumu

* sudo apt-get install phpmyadmin
* sudo php5enmod mcrypt
* sudo service php5-fpm restart

**Eğer 6. aşamadaki root klasörü değiştirme işlemi yaptıysanız**

* sudo ln -s /usr/share/phpmyadmin /home/username/php


