# Web Stack Implementation (Lamp Stack) in AWS

# Step 1 : Installing Apache and Updating the Firewall ; Apche HTTP Server is the most widely used web server software.

## Install Apache using Ubuntu's package manager 'apt' with the followin code:
`sudo apt update` 

![Alt text](<images/sudo apt update.png>)

`sudo apt install apache2`

![Alt text](<images/sudo apt install apache2.png>)

## To verify that apache2 is running as a service in our OS, use following command:
`sudo systemctl status apache2`

![Alt text](<images/sudo status.png>)

## Use the curl command to make sure that our Apache web service responds to 'curl'
`curl http://localhost:80`

`curl -s http://169.254.169.254/latest/meta-data/public-ipv4`

![Alt text](<images/curl command.png>)

## If you see the page below, that means your web server is now correctly installed and accessible through your firewall.

![Alt text](<images/Apache2 default page.png>)


# Step 2: Installing MySQL
### *MySQL is a popular relational database management system used within PHP environments.*

## Again, use 'apt' to acquire and install this software:
`sudo apt install mysql-server`

![Alt text](<images/install mysql.png>)

## When the installation is finished, log in to the MySQL console by typing:
`sudo mysql`

![Alt text](<images/mysql console.png>)

## It's recommended that you run a security script that comes pre-installed with MySQL, with the following commands:
`ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';`

`mysql> exit`

![Alt text](<images/alter user and exit.png>)
## Now start the interactive script by running:
`$ sudo mysql_secure_installation`

![Alt text](<images/setting password.png>)

## When that is done, the next step is to test if we can be able to login into the MySQL console with this command:
`sudo mysql-p`

![Alt text](<images/login into mysql.png>)

# Step 3: Installing PHP
## PHP is the component of our setup that will process code to display dynamic content to the end user.

## Firstly, install PHP using `sudo apt install php`

![Alt text](<images/install php.png>)

## Then install php-mysql ; a module that allows PHP to communicate wit MYSQL-based databases, using `sudo apt install php-mysql`

![Alt text](<images/install php-mysql.png>)

## Lastly, install libapache2 so as to enable Apache to handle PHP files, using `sudo apt install libapache2-mod-php`

![Alt text](<images/install libapache2.png>)

## Once the installation is finished, you can confirm the version of the PHP using `php -v`

![Alt text](<images/php version.png>)

# Step 4: Creating a Virtual Host for your Website using Apache.

## Creating a directory for projectlamp using 'mkdir'
`$ sudo mkdir /var/www/projectlamp`

`$ sudo chown -R $USER:$USER /var/www/projectlamp`

`$ sudo vi /etc/apache2/sites-available/projectlamp.conf`

`http://<Public-IP-Address>:80`

## Now go to your browser and try to open your website URL using IP address.

![Alt text](<images/hello lamp.png>)

# Step 5: Enable PHP on the website

`sudo vim /etc/apache2/mods-enabled/dir.conf`

`$ vim /var/www/projectlamp/index.php`

`<?php phpinfo();`

## When are you finished, save and close the file, refresh the page and you will see  page similar to this:

![Alt text](<images/php landing page.png>)


