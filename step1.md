# STEP 1 — INSTALLING APACHE AND UPDATING THE FIREWALL

## Install Apache using Ubuntu’s package manager ‘apt’

Run the commands below inside your Ubuntu instance via ssh command line
```
#update a list of packages in package manager
sudo apt update

#run apache2 package installation
sudo apt install apache2
```

## Verify that apache2 is running as a Service in our OS

```
sudo systemctl status apache2
```

![validation of apache2](./images/Validate%20Apache2%20service.png)

Validate if Apache HTTP server can respond to requests from the Internet.

1. Check public IP address in AWS Web console

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![AWS public ip address](./images/aws%20public%20address.png)


2. Open browser of choice and try to access the following URL
    ```
    http://<Public-IP-Address>:80
    ```
3. It is now good if you can access it.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![apache browser](./images/Apache%20browser.png) 

