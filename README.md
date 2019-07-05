# vhost-xampp

## Edit the following files like sample files

### C:\Windows\System32\drivers\etc\hosts

register local server directory
```html
127.0.0.1       	localhost
::1             	localhost

127.0.0.1		test.test
```

### C:\xampp\apache\conf\httpd.conf

allow access to the httpd-vhosts.conf file on line 520, remove #

```html
# Virtual Hosts
Include conf/extra/httpd-vhosts.conf
```

### C:\xampp\apache\conf\extra\httpd-vhosts.conf
register localhost first and test local server as following
```php
<VirtualHost *:80>
     ServerName localhost
     DocumentRoot "C:/xampp/htdocs"
</VirtualHost>

<VirtualHost *:80>
    ServerName test.test
    DocumentRoot "E:/my/project/Test"
    <Directory E:/my/project/Test>  
        AllowOverride none
        Require all granted  
    </Directory>
</VirtualHost>
```

## Restart Xampp and Enjoy!!!
