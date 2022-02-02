# Centralized Management Solutions 5.x

**Configurations:**

````
npm install -g @angular/cli
npm install -g gulp
npm install -g tslint
npm install -g typescript
````

````
Add the PATH system variable
<project-folder>\bin (e.g: D:\Projects\cms\bin)
````

````
_../php.ini_
[Xdebug]
zend_extension="D:/Servers/xampp/php/ext/php_xdebug-2.9.2-7.4-vc15-x86_64.dll"
xdebug.remote_enable = On
xdebug.profiler_enable = Off
xdebug.profiler_enable_trigger = Off
xdebug.profiler_output_name = cachegrind.out.%t.%p
xdebug.profiler_output_dir ="D:/Servers/xampp/tmp"
xdebug.show_local_vars=0

[cms]
...
extension=php_phalcon.dll
extension=php_psr.dll
extension=php_apcu.dll
extension=php_ds.dll
extension=php_mongodb.dll
````

````
_../httpd-vhosts.conf_
<VirtualHost *:80>
  ServerName localhost
  ServerAlias localhost
  DocumentRoot "D:/projects/cms.pro.vn"
  <Directory  "D:/projects/cms.pro.vn/">
    Options +Indexes +Includes +FollowSymLinks +MultiViews
    AllowOverride All
    Require all granted
  </Directory>
</VirtualHost>

<VirtualHost *:8080>
  ServerName localhost:8080
  ServerAlias localhost:8080
  DocumentRoot "D:/Servers/xampp/htdocs"
  <Directory "D:/Servers/xampp/htdocs/">
    Options +Indexes +Includes +FollowSymLinks +MultiViews
    AllowOverride All
    Require all granted
  </Directory>
</VirtualHost>

<VirtualHost *:80>
	ServerName dev.cms.com
	DocumentRoot "D:/projects/cms"
	<Directory  "D:/projects/cms/">
		Options +Indexes +Includes +FollowSymLinks +MultiViews
		AllowOverride All
		Require local
	</Directory>
</VirtualHost>

<VirtualHost *:80>
	ServerName admin.cms.com
	DocumentRoot "D:/projects/cms"
	<Directory  "D:/projects/cms/">
		Options +Indexes +Includes +FollowSymLinks +MultiViews
		AllowOverride All
		Require local
	</Directory>
</VirtualHost>

<VirtualHost *:80>
	ServerName template.cms.com
	DocumentRoot "D:/projects/cms"
	<Directory  "D:/projects/cms/">
		Options +Indexes +Includes +FollowSymLinks +MultiViews
		AllowOverride All
		Require local
	</Directory>
</VirtualHost>

<VirtualHost *:80>
	ServerName install.cms.com
	DocumentRoot "D:/projects/cms"
	<Directory  "D:/projects/cms/">
		Options +Indexes +Includes +FollowSymLinks +MultiViews
		AllowOverride All
		Require local
	</Directory>
</VirtualHost>

<VirtualHost *:80>
	ServerName account.cms.com
	DocumentRoot "D:/projects/cms"
	<Directory  "D:/projects/cms/">
		Options +Indexes +Includes +FollowSymLinks +MultiViews
		AllowOverride All
		Require local
	</Directory>
</VirtualHost>

<VirtualHost *:80>
	ServerName store.cms.com
	DocumentRoot "D:/projects/cms"
	<Directory  "D:/projects/cms/">
		Options +Indexes +Includes +FollowSymLinks +MultiViews
		AllowOverride All
		Require local
	</Directory>
</VirtualHost>

<VirtualHost *:80>
	ServerName profile.cms.com
	DocumentRoot "D:/projects/cms"
	<Directory  "D:/projects/cms/">
		Options +Indexes +Includes +FollowSymLinks +MultiViews
		AllowOverride All
		Require local
	</Directory>
</VirtualHost>
````

````
_C:\Windows\System32\drivers\etc\hosts_
127.0.0.1 localhost
::1 localhost
127.0.0.1	admin.cms.com
::1	admin.cms.com
127.0.0.1	dev.cms.com
::1	dev.cms.com
127.0.0.1	template.cms.com
::1	template.cms.com
127.0.0.1	install.cms.com
::1	install.cms.com
127.0.0.1	account.cms.com
::1	account.cms.com
127.0.0.1	store.cms.com
::1	store.cms.com
127.0.0.1	profile.cms.com
::1	profile.cms.com
````
