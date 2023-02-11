---
Title: "Installing SugarCRM on Ubuntu using LAMP"
description: "Learn how to install SugarCRM on Ubuntu and run it on a local host using the LAMP stack."
dateString: February 2023
draft: false
tags: ["SugarCRM", "LAMP", "Ubuntu", "Installation", "Localhost"]
weight: 103
cover:
    image: "/blog/sugarcrm-lamp-installation/cover.png"
---

# Introduction

SugarCRM is a popular customer relationship management (CRM) platform that helps businesses manage customer data and interactions. In this tutorial, you'll learn how to install SugarCRM on Ubuntu and run it on a local host using the LAMP stack (Linux, Apache, MySQL, and PHP).

# Prerequisites

Before you begin, make sure you have the following:

A running Ubuntu system
Access to the terminal
Administrative privileges (sudo access)

# Step 1: Update Ubuntu
Before installing any new software, it's always a good idea to update your system. Run the following command to update Ubuntu:

```
sudo apt-get update
```

# Step 2: Install Apache
Apache is the web server that will host your SugarCRM installation. Run the following command to install Apache:

```
 sudo apt-get install apache2
```

# Step 3: Install MySQL
MySQL is the database management system that SugarCRM will use to store its data. Run the following command to install MySQL:

```
sudo apt-get install mysql-server
```
# Step 4: Secure MySQL
It's important to secure your MySQL installation by running the following command:

```
sudo mysql_secure_installation
```
# Step 5: Install PHP
SugarCRM is built using PHP, so you'll need to install PHP and the necessary modules. Run the following command to install PHP and its modules:

```
sudo apt-get install php php-common php-mbstring php-xmlrpc php-soap php-gd php-xml php-intl php-mysql
```
# Step 6: Configure Apache for PHP
You need to configure Apache to use PHP. Run the following command to enable the php module:

```
sudo a2enmod php7.4
```
# Step 7: Restart Apache
After enabling the php module, you need to restart Apache for the changes to take effect. Run the following command to restart Apache:

```
sudo service apache2 restart
```
# Step 8: Download SugarCRM
Download the latest version of SugarCRM from the official website and extract the contents to the Apache document root directory (/var/www/html).

# Step 9: Create a MySQL Database for SugarCRM
Create a new database for SugarCRM using the following commands:

```
mysql -u root -p
CREATE DATABASE sugarcrm;
GRANT ALL PRIVILEGES ON sugarcrm.* TO 'sugarcrm'@'localhost' IDENTIFIED BY 'password';
FLUSH PRIVILEGES;
EXIT;
```
# Step 10: Configure SugarCRM
Point your web browser to http://localhost/sugarcrm to access the SugarCRM installation wizard. Follow the steps to configure SugarCRM, providing the database information you created in step 9.

That's it! You should now have SugarCRM installed and running on your local host. You can log in to the application using the username and password you specified during the installation process.

I hope this tutorial helps you successfully install SugarCRM on Ubuntu using the LAMP