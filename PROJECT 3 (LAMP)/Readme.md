# LAMP - Linux, Apache, MySQL, PHP or Python, or Perl

## Prerequisites;
- AWS free tier account(This has been created already).
- EC2 instance connected and running on ssh.
- Windows Powershell downloaded and connected to  instance by running the PEM key.


## Using PEM key to connect to EC2 instance via windows powershell
- `InstanceConnection (1)` and `InstanceConnection (2)`(***cd download***) : This command was used to move into the into the downloads folder
- `InstanceConnection (1)` and `InstanceConnection (2)` (***ssh -i lamp&lemp.pem ubuntu@x4.xx3.1xx.xx0***) : This command was used to connect the PEM key to the EC2 instance using the windows powershell. although the initial command didnt work as i had to wrap  the ampersand(&) in double quotation marks ("&") so i used this command (***ssh -i lamp"&"lemp.pem ubuntu@4.xx3.1xx.xx0***)
![`EC2Running`](Images/EC2Running.PNG)
![`InstanceConnection (1)`](<Images/InstanceConnection (1).PNG>)
![`InstanceConnection (2)`](<Images/InstanceConnection (2).PNG>)



## Installing Apache and Updating the Firewall
Apache is an open source software available for free. it runs on 67% of all webserves in the world. It is fast, reliable, and secure. it can be highly customized to meet the needs of many diiferent environments by using extensions and modules. Most WordPress hosting providers use Apache as their web server software, websites and other applications can run on other web server software as well as Nginx, Microsoft IIS, etc. The following command was used.

- `SudoAptUpdate (1)` `SudoAptUpdate (2)` and `SudoAptUpdate (3)` (***$ sudo apt update***) : This command was used to update a list of packages
- `SudoAptInstallApache2 (1)` `SudoAptInstallApache2 (2)` and `SudoAptInstallApache2 (3)` (***$ sudo apt install apache2 -y***) : This command was used to run apache2 package installation
- `SudoSystemctlStatusApache2` (***$ sudo systemctl status apache2***) : This command was used to verify that Apache is running using. If it is green and running that means that the apache was installed correctly.
- `CurlWebAccess (1)` `CurlWebAccess (2)` and `CurlWebAccess (3)`(***$ curl http://localhost:80***) : This command was used to request the apache HTTP Server on port 80 using the DNS name and this can be pasted on your web browser to enable it display the Ubuntu Apache2 default page

![`SudoAptUpdate (1)`](<Images/SudoAptUpdate (1).PNG>)
![`SudoAptUpdate (2)`](<Images/SudoAptUpdate (2).PNG>)
![`SudoAptUpdate (3)`](<Images/SudoAptUpdate (3).PNG>)

![`SudoAptInstallApache2 (1)`](<Images/SudoAptInstallApache2 (1).PNG>)
![`SudoAptInstallApache2 (2)`](<Images/SudoAptInstallApache2 (2).PNG>)
![`SudoAptInstallApache2 (3)`](<Images/SudoAptInstallApache2 (3).PNG>)

![`SudoSystemctlStatusApache2`](Images/SudoSystemctlStatusApache2.PNG)

![`CurlWebAccess (1)`](<Images/CurlWebAccess (1).PNG>)
![`CurlWebAccess (2)`](<Images/CurlWebAccess (2).PNG>)
![`CurlWebAccess (3)`](<Images/CurlWebAccess (3).PNG>)
![`UbuntuApache2Default page`](<Images/UbuntuApache2Default page.PNG>)



## Installing MySQL
MySQL is a popular database management system used within PHP environments
- `InstallMySQLserver (1)` `InstallMySQLserver (2)` `InstallMySQLserver (3)` `InstallMySQLserver (4)` and `InstallMySQLserver (5)`(***$ sudo apt install mysql-server***) : This command was used to install the software.

- `ConnectingSQLnativePasswordAndExit`(***$ sudo mysql***) : When the above is done installing this command was used to log in to the MySQL console. This will connect to the MySQL server as the administrative database user root, which is inferred by the use of sudo when running this command. it's recommended that you run a security script that comes pre-installed with MySQL. This script will remove some insecure default settings and lock down access to your database system. Before running the script you will set a password for the root user, using ***mysql_native_password*** as default authentication method. This command was used for it ***mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';***. ***mysql> exit*** can be used to exit MySQL shell.

- `MySQLSecureInstallationWithPASSWORDchange` (***$ sudo mysql_secure_installation***) : This command can be used to start the interactive script. This will ask if you want to configure the ***VALIDATE PASSWORD PLUGGIN***, please note that if you leave validation disabled and you run ***sudo mysql*** and input the native password you used, you may get an error feedback like ***ERROR 1045 (28000): Access denied for user 'root'@'localhost' (using passowrd: password)*** so its advisable you enable ***VALIDATE PASSWORD PLUGIN*** and enter 2 for strongest level as you will receive errors when attempting to set any password which does not contain a mix of uppercase, lowercase, special characters and number or which is based on common dictionary words e.g PassWord.1 will not be rejected by MySQL with an error and also answer Y for yes for the rest of the questions and hit enter. When you set up the ***VALIDATE PASSWORD PLUGIN***, your server will ask you to select and confirm a password for the MySQL root user. The database root user is an administrative user with full privileges over the database system.

- `MySQLtestLoginwithChangedPassword`(***$ sudo mysql -p***) : This command was used to test if one is able to log into the MySQL console, -p flag in this command will prompt you for the password used after changing the root user password and to exit the MySQL console for this you will use the password you created in the above step, type ***mysql> exit***


![`InstallMySQLserver (1)`](<Images/InstallMySQLserver (1).PNG>)
![`InstallMySQLserver (2)`](<Images/InstallMySQLserver (2).PNG>)
![`InstallMySQLserver (3)`](<Images/InstallMySQLserver (3).PNG>)
![`InstallMySQLserver (4)`](<Images/InstallMySQLserver (4).PNG>)
![`InstallMySQLserver (5)`](<Images/InstallMySQLserver (5).PNG>)

![`ConnectingSQLnativePasswordAndExit`](Images/ConnectngSQLnativePasswordAndExit.PNG)

![`MySQLSecureInstallationWithPASSWORDchange`](Images/MySQLSecureInstallationWithPASSWORDchange.PNG)

![`MySQLtestLoginwithChangedPassword`](Images/MySQLtestLoginwithChangedPassword.PNG)



## Installing PHP
PHP is the component of our setup that will process code to display dynamic content to the end user.

- ***$ sudo apt install php libapache2-mod-php php-mysql*** : This command was used to enable apache to handle PHP files. Core PHP packages will automatically be installed as dependencies.


- ***php -v*** : This command was used to confirm the PHP version that was installed

![`InstallPHPandDependencies (1)`](<Images/InstallPHPandDependencies (1).PNG>)
![`InstallPHPandDependencies (2)`](<Images/InstallPHPandDependencies (2).PNG>)
![`InstallPHPandDependencies (3)`](<Images/InstallPHPandDependencies (3).PNG>)
![`php-v`](Images/php-v.PNG)


## Enabling PHP on the website
With the default DirectoryIndex settings on Apache, a file named index.html will always take precedence over an index.php file. This is useful for setting up maintenance pages in PHP applications, by creating a temporary index.html file containing an informative message to visitors. Because this page will take precedence over the index.php page, it will then become the landing page for the application. once maintenance is over, the index.html is renamed or removed from the document root, bringing back the regular apllication page.

- ***sudo vim /etc/apache2/mods-enabled/dir.conf*** : This command was used to edit the vim text editor and change the order in which the index.php file is listed within the DirectoryIndex directive. Using the below.
<IfModule mod_dir.c>
        #Change this:
        #DirectoryIndex index.html index.cgi index.pl index.php index.xhtml index.htm
        #To this:
        DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm
</IfModule>.


- ***$ sudo systemctl reload apache2*** : This command was used reload Apache so the above changes can take effect.

- `projectlamp` (***$ nano /var/www/projectlamp/index.php***) : This command was used to create a new file named index.php inside the customer web root folder as a PHP script will be used to test that Php is correctly installed and configured on the server, and also to confirm that Apache is able to handle and process requestd for PHP files. the PHP code below is to be pasted in the blank nano text editor
<?php
phpinfo();



![`SudovimetcApache2modsenableddir.conf`](Images/SudovimetcApache2modsenableddir.conf.PNG)
![`ChangePHPhomepage`](Images/ChangePHPhomepage.PNG)
![`sudo reload`](<Images/sudo reload.PNG>)
!['projectlamp'](Images/projectlamp.PNG)
![`PHPCodeUsedInNanoTextEditorForPHPLandingpage`](Images/PHPCodeUsedInNanoTextEditorForPHPLandingpage.PNG)