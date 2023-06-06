# STEP 4- CREATING A VIRTUAL HOST FOR YOUR WEBSITE USING APACHE

## Setup a domain called projectlamp

Create the directory for projectlamp using ‘mkdir’ command as follows:
```
sudo mkdir /var/www/projectlamp
``` 
Next, assign ownership of the directory with your current system user:
```
sudo chown -R $USER:$USER /var/www/projectlamp
```
![projectlamp-directory](./images/projectlamp%20directory.png)

## Create a new configuration file in Apache's sites-available directory

```
sudo vi /etc/apache2/sites-available/projectlamp.conf
```
This will create a blank page. Paste the following below.
```
<VirtualHost *:80>
    ServerName projectlamp
    ServerAlias www.projectlamp 
    ServerAdmin webmaster@localhost
    DocumentRoot /var/www/projectlamp
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```
![apache config](./images/validate%20apache%20config.png)

Run the following commands below to enable new virtual host, disable default website from Apache, validate file doesn't have syntax error and reload Apache for changes to take effect:

```
sudo a2ensite projectlamp
sudo a2dissite 000-default
sudo apache2ctl configtest
sudo systemctl reload apache2
```

Go to browser to check if Apache virtual host is working.

![virtual host running](./images/Apache%20virtual%20host.png)

