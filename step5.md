# STEP 5 - ENABLE PHP ON WEBSITE
## List index.php file within the DirecotryIndex directive
```
sudo vim /etc/apache2/mods-enabled/dir.conf
```
```
<IfModule mod_dir.c>
        #Change this:
        #DirectoryIndex index.html index.cgi index.pl index.php index.xhtml index.htm
        #To this:
        DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm
</IfModule>
```
Reload Apache after saving
```
sudo systemctl reload apache2
```
## Create a new file name index.php and add the following text

```
vim /var/www/projectlamp/index.php
```
This will open a blank file and add the following text
```
<?php
phpinfo();
```

When finished, access Apache virtual host thru browser and should look like these.
![php validation](./images/php%20validation.png)