# LAMP Installation Guide

The following guide will show how to install LAMP enviroment in Ubuntu 16.04.

## Getting Started


### Prerequisites

Make sure your packages and system are updated.

To update all the installed packages just execute the following command:

```
sudo apt update
```

Then execute: 

```
sudo apt upgrade
```

##

### Installing

Once all our packages are updated we can proceed with the installation.

### Step 1 — Installing Apache

We are going to install apache service first, this can be done by running: 


```
sudo apt install apache2
```


After running the previous command, you should be able to do: http://your_server_ip, an info page would be showed with the information of your Apache server.

##

### Step 2 — Installing MySQL

As our database service we are going install mysql service. Run the following command: 

```
sudo apt install mysql-server
```

While installing a prompt will be displayed, it will ask for a password and then a confirmation of that password.

After installing mysql, you can run the following: 

```
mysql -uroot -p[your password]   
```
To verify if the installation was succesfull.

##

### Step 3 — Installing PHP

PHP is a server scripting language, and a powerful tool for making dynamic and interactive Web pages.
To install it just run: 

```
sudo apt install php libapache2-mod-php php-mysql
```

Notice that **libapache2-mod-php php-mysql** are some required dependencies to install along PHP.


##

## Step 4 — Testing PHP Processing on your Web Server

In order to test that your system is configured properly for PHP, create a very basic PHP script called info.php. In order for Apache to find this file and serve it correctly, it must be saved to a very specific directory, which is called the "web root".

In Ubuntu 16.04, this directory is located at /var/www/html/. Create the file at that location by running:

```
sudo nano /var/www/html/info.php
```

This will open a blank file. Add the following text, which is valid PHP code, inside the file:

```
<?
php
phpinfo();
?>
```

Now go to: http://your_server_ip/info.php

The page that you come to should look something like this:

![Alt](https://www.hugeserver.com/kb/wp-content/uploads/2017/01/php7infodebian.png) 

## Authors

* **Warren Carvajal** - *IMPROVE* - [https://github.com/kagebushin17
](https://github.com/kagebushin17)

