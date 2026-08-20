# Apache Web Server & Portfolio Hosting

This section covers the basic setup and management of the Apache HTTP Server on an Ubuntu Linux virtual machine and demonstrates how a personal portfolio website can be hosted using Apache.

---

## 1. Update Package Information

Before installing Apache, update the package index:


bash
sudo apt update


## 2. Install Apache
Install the Apache HTTP Server:
sudo apt install apache2

# Verify the installation:
apache2 -v


## 3. Check Apache Service Status
Check whether Apache is running:

sudo systemctl status apache2

A successfully running Apache service should show:
active (running)


## 4. Start Apache
If Apache is not running:
sudo systemctl start apache2

#Check its status:
sudo systemctl status apache2


## 5. Enable Apache at Boot
Configure Apache to start automatically when the system boots:
sudo systemctl enable apache2

#Verify:
systemctl is-enabled apache2


## 6. Restart Apache
Restart Apache after making configuration changes:
sudo systemctl restart apache2


## 7. Apache Web Root
On Ubuntu, the default Apache web root is:
/var/www/html

The default web page is:
/var/www/html/index.html

The contents of this directory are served by Apache.


## 8. Create a Simple Web Page
Navigate to the Apache web root:
cd /var/www/html

#Create or edit the main web page:
sudo nano index.html

#A simple example:
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Linux Hosted Portfolio</title>
</head>
<body>

    <h1>Welcome to My Portfolio</h1>
    <p>This website is hosted on an Ubuntu Linux VM using Apache.</p>

</body>
</html>


## 9. Access the Website
Find the IP address of the Ubuntu VM:

ip addr
or:
hostname -I

Then open the VM's IP address in a web browser:
http://VM-IP-ADDRESS

#For example:
http://192.168.1.100

If Apache is running correctly and network access is configured, the portfolio website should be displayed.


## 10. Deploy an Existing Portfolio
An existing HTML/CSS/JavaScript portfolio can be copied into the Apache web root:
sudo cp -r /path/to/portfolio/* /var/www/html/

# Alternatively, the existing files can be placed directly inside:
/var/www/html/

The main page should normally be named:
index.html


## 11. Check Apache Configuration
Apache configuration files are located under:
/etc/apache2/

# The main configuration file is:
/etc/apache2/apache2.conf

Virtual host configurations are stored in:
/etc/apache2/sites-available/

Enabled virtual hosts are linked under:
/etc/apache2/sites-enabled/


## 12. Test Apache Configuration
Before restarting Apache after configuration changes:
sudo apache2ctl configtest

# A successful configuration test should return:
Syntax OK


## 13. View Apache Logs
Apache logs can be useful when troubleshooting.

Access log
sudo tail -f /var/log/apache2/access.log

Error log
sudo tail -f /var/log/apache2/error.log

Press:
Ctrl + C

to stop following the log.



## 14. Common Apache Commands
sudo systemctl start apache2
sudo systemctl stop apache2
sudo systemctl restart apache2
sudo systemctl reload apache2
sudo systemctl enable apache2
sudo systemctl disable apache2
sudo systemctl status apache2


# 🔄 Apache Hosting Workflow
Ubuntu Linux VM
       ↓
Update package index
       ↓
Install Apache
       ↓
Start Apache service
       ↓
Enable Apache at boot
       ↓
Place portfolio files in /var/www/html
       ↓
Test Apache configuration
       ↓
Access portfolio using VM IP


#📌 Important Paths


Path                                       Purpose

/var/www/html                              Default Apache web root

/etc/apache2/                              Apache configuration directory

/etc/apache2/apache2.conf                  Main apache configuration

/etc/apache2/sites-available/              Available virtual host configuration

/etc/apache2/sites-enabled/                Enabled virtual host configurations

/var/log/apache2/access.log                Apache access log

/var/log/apache2/error.log                 Apache error log
