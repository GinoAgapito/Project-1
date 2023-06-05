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