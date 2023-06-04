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
