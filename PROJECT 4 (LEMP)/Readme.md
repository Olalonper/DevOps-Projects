# WEB STACK IMPLEMENTATION FOR LEMP STACK- Linux, Nginx, MySQL, PHP or Python, or Perl

## Prerequisites needed to ;
- AWS free tier account(This has been created already).
- EC2 instance connected and running on git bash.
- Git bash downloaded and connected to  instance by running the PEM key.


## EC2 running on AWS
- `EC2Running` : This image shows the Lemp instance already up and running (P.S the ip address was covered for security reasons).
    - see image `EC2 instance` below :point_down:![`EC2 instance`](<Images/EC2 instance.PNG>)


## Using PEM key to connect to EC2 instance via git bash
For this to be connected successfully the below command needs to run;
- ***cd download*** : This command was used to move into the into the downloads folder as this is folder the PEM key was stored in.
    - see image `cd downloads` below :point_down:![`cd downloads`](<Images/cd downloads.PNG>)

- ***ssh -i Lamp&Lemp.pem ubuntu@1x.2xx.xx9.x2*** : This command was used to connect the PEM key to the EC2 instance using the git bash. please note that you are to wrap the ampersand(&) in double quotation marks ("&") so i used this command (***ssh -i Lamp"&"Lemp.pem ubuntu@1x.2xx.xx9.x2***).
    - see image `connecting pem key to gitbash` below :point_down:![`connecting pem key to gitbash`](<Images/connecting pem key to gitbash.PNG>)


## Installing the Nginx Web Server
### Step 1
In order to display web pages to our site visitors, we are going to employ Nginx, a high-performance web werver. we'll uste the ***apt*** package manager to install this package. Since this is our first time using ***apt*** for this session, we need to start off by updating the server's package index. Following that, you can use ***apt Install*** to get Nginx istalled run the following commands below.

- ***$ sudo apt update*** : This command was used to update a list of packages.
    - see image `sudo apt update` below :point_down:![`sudo apt update`](<Images/sudo apt update.PNG>)

- ***$ sudo apt install nginx*** : This command was used to install Nginx package installation.
    - see image `sudo apt install nginx1` below :point_down:![`sudo apt install nginx1`](<Images/sudo apt install nginx1.PNG>)
    - see image `sudo apt install nginx2` below :point_down:![`sudo apt install nginx2`](<Images/sudo apt install nginx2.PNG>)
    - see image `sudo apt install nginx3` below :point_down:![`sudo apt install nginx3`](<Images/sudo apt install nginx3.PNG>)



- ***$ sudo systemctl status nginx*** : This command was used to verify that Apache is running using. If it is green and running that means that the apache was installed correctly.
    - see image `sudo systemctl status nginx` below :point_down:![`sudo systemctl status nginx`](<Images/sudo systemctl status nginx.PNG>)
    
    
- ***$ curl http://localhost:80*** : The ***curl*** command when run will return strangely formatted texts basically a bunch of html codes, but not cause for alarm its just to make sure that the Nginx web service responds to ***curl*** command with some payload.
    - see image `curl web access nginx` below :point_down:![`curl web access nginx`](<Images/curl web access nginx.png>)

- OR you can copy the IP address and paste it on your browser to confim that Nginx works correctly. either you do the above or below you should get the below in your web browser.
    - see image `testing nginx server from the web browser` below :point_down:![`testing nginx server from the web browser`](<Images/testing nginx server from the web browser.PNG>)


    ## Installing MySQL
    ### Step 2
MySQL is a popular database management system used within PHP environments. Now that the web server is up and running, you need to intall a Database Management System (DBMS) to be able to store and manage datta for the site in a relational database.
- ***$ sudo apt install mysql-server***: This command was used to install the software.
    - see image `sudo apt install mysql-server1` below :point_down:![`sudo apt install mysql-server1`](<Images/sudo apt install mysql-server1.PNG>)
    - see image `sudo apt install mysql-server2` below :point_down:![`sudo apt install mysql-server2`](<Images/sudo apt install mysql-server2.PNG>)
    - see image `sudo apt install mysql-server3` below :point_down:![`sudo apt install mysql-server3`](<Images/sudo apt install mysql-server3.PNG>)
    - see image `sudo apt install mysql-server4` below :point_down:![`sudo apt install mysql-server4`](<Images/sudo apt install mysql-server4.PNG>)


- ***$ sudo mysql*** : When the above is done installing this command was used to log in to the MySQL console. This will connect to the MySQL server as the administrative database user root, which is inferred by the use of sudo when running this command. it's recommended that you run a security script that comes pre-installed with MySQL. This script will remove some insecure default settings and lock down access to your database system. Before running the script you will set a password for the root user, using ***mysql_native_password*** as default authentication method. This command was used for it ***mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';***. ***mysql> exit*** can be used to exit MySQL shell.
    - see image `sudo mysql setting native password` below :point_down:![`sudo mysql setting native password`](<Images/sudo mysql setting native password.PNG>)


- ***$ sudo mysql_secure_installation*** : This command can be used to start the interactive script. This will ask if you want to configure the ***VALIDATE PASSWORD PLUGGIN***, please note that if you leave validation disabled and you run ***sudo mysql*** and input the native password you used, you may get an error feedback like ***ERROR 1045 (28000): Access denied for user 'root'@'localhost' (using passowrd: password)*** so its advisable you enable ***VALIDATE PASSWORD PLUGIN*** and enter 2 for strongest level as you will receive errors when attempting to set any password which does not contain a mix of uppercase, lowercase, special characters and number or which is based on common dictionary words e.g PassWord.1 will not be rejected by MySQL with an error and also answer Y for yes for the rest of the questions and hit enter. When you set up the ***VALIDATE PASSWORD PLUGIN***, your server will ask you to select and confirm a password for the MySQL root user. The database root user is an administrative user with full privileges over the database system. Please that when typing the passowrd it doesnt show so one has to be very careful when typing.
    - see image `sudo mysql secure installation1` below :point_down:![`sudo mysql secure installation1`](<Images/sudo mysql secure installation1.PNG>)
    - see image `sudo mysql secure installation2` below :point_down:![`sudo mysql secure installation2`](<Images/sudo mysql secure installation2.PNG>)

- ***$ sudo mysql -p*** : This command was used to test if one is able to log into the MySQL console, -p flag in this command will prompt you for the password used after changing the root user password and to exit the MySQL console for this you will use the password you created in the above step, type ***mysql> exit***.
    - see image `sudo mysql -p` below :point_down:![`sudo mysql -p`](<Images/sudo mysql -p.PNG>)


## Installing PHP
### Step 3
While Apache embeds the PHP interpreter in each request, Nginx requires an external program to handle PHP processing and act as a bridge between the PHP interpreter itself and the web server. This allows for a better overall performance in most PHP-based websites, but it requires additional configuration. one will need to install ***phfpm***, which stands for "PHP fastCGI process manager", and tell Nginx to pass PHP requests to this software for processing. Additionally, you'll need ***php-mysql***, a PHP module that allows PHP to communicate with MySQL-based databases. Core PHP packages will automatically be installed as dependencies.

- `installing php1`***$ sudo apt install php-fpm php-mysql*** : This command was used to enable apache to handle PHP files. Core PHP packages will automatically be installed as dependencies.
    - see image `InstallPHPandDependencies (1)` below :point_down:![`installing php1`](<Images/installing php1.PNG>)
    - see image `InstallPHPandDependencies (2)` below :point_down:![`installing php2`](<Images/installing php2.PNG>)
    - see image `InstallPHPandDependencies (3)` below :point_down:![`installing php3`](<Images/installing php3.PNG>)

- ***php -v*** : This command was used to confirm the PHP version that was installed.
    - ![`php-v`](Images/php-v.PNG)


## Enabling PHP on the website
With the default DirectoryIndex settings on Apache, a file named index.html will always take precedence over an index.php file. This is useful for setting up maintenance pages in PHP applications, by creating a temporary index.html file containing an informative message to visitors. Because this page will take precedence over the index.php page, it will then become the landing page for the application. once maintenance is over, the index.html is renamed or removed from the document root, bringing back the regular apllication page.

- ***sudo vim /etc/apache2/mods-enabled/dir.conf*** : This command was used to edit the vim text editor and change the order in which the index.php file is listed within the DirectoryIndex directive, using the code in the nano text editior.
    - see image `SudovimetcApache2modsenableddir.conf` below :point_down:![`SudovimetcApache2modsenableddir.conf`](Images/SudovimetcApache2modsenableddir.conf.PNG)
    - see image `ChangePHPhomepage` below :point_down:![`ChangePHPhomepage`](Images/ChangePHPhomepage.PNG)


- ***$ sudo systemctl reload apache2*** : This command was used reload Apache so the above changes can take effect.![`sudo reload`](<Images/sudo reload.PNG>)


- ***$ nano /var/www/projectlamp/index.php*** : This command was used to create a new file named index.php inside the customer web root folder as a PHP script will be used to test that Php is correctly installed and configured on the server, and also to confirm that Apache is able to handle and process requestd for PHP files. the PHP code is pasted in the nano text editor.
    - !['projectlamp'](Images/projectlamp.PNG)
    - see image `PHPCodeUsedInNanoTextEditorForPHPLandingpage` below :point_down:![`PHPCodeUsedInNanoTextEditorForPHPLandingpage`](Images/PHPCodeUsedInNanoTextEditorForPHPLandingpage.PNG)



## Creating a Virtual Host for your Website using Apache
- ***$ sudo mkdir /var/www/projectlamp*** : This command was used to create the directory for ***projectlamp***.
    - see image `CreatedDirectoryforProjectLAMP` below :point_down:![`CreatedDirectoryforProjectLAMP`](Images/CreatedDirectoryforProjectLAMP.PNG)


- ***$ sudo chown -R $USER:$USER /var/www/projectlamp*** : This command was used to assign ownership of the directory with the ***$USER*** environment variab, which will reference the current system user.
    - see image `AssignedOwnershipWithThe$USER` below :point_down:![`AssignedOwnershipWithThe$USER`](Images/AssignedOwnershipWithThe$USER.PNG)

- ***$ sudo vi /etc/apache2/sites-available/projectlamp.conf*** `PHPlampProjectConfig (1)` `PHPlampProjectConfig (1)`: This command was used create and open a new configuration in Apache's ***sites-available*** directory using any preferred command-line editor in this case vi was used. The virtual host code was pasted in blank vi text editor.
- ***$ sudo ls /etc/apache2/sites-available*** `PHPlampProjectConfig (1)` `PHPlampProjectConfig (1)`: This command was used to show the new file in the ***sites-available*** directory You will see something like this 000-default.conf  default-ssl.conf  projectlamp.conf
- ***$ sudo a2ensite projectlamp*** `PHPlampProjectConfig (1)` `PHPlampProjectConfig (1)`: This command was used to enable the new virtual host.
- ***$ sudo a2dissite 000-default*** `PHPlampProjectConfig (1)` `PHPlampProjectConfig (1)`: This command was used to disable the defaukt website that comes installed with Apache. This is required if you're not using a custom domain name, because in this case Apache's default configuration would overwrite the virtual host.
- ***$ sudo apache2ctl configtest*** `PHPlampProjectConfig (1)` `PHPlampProjectConfig (1)`: This command was used to make sure the configuration file doesnt contain syntax errors.
- ***$ sudo systemctl reload apache2*** `PHPlampProjectConfig (1)` `PHPlampProjectConfig (1)`: This command was used to reload Apache so the changes take effect.
    - see image `PHPlampProjectConfig (1)` below :point_down:![`PHPlampProjectConfig (1)`](<Images/PHPlampProjectConfig (1).PNG>)
    - see image `PHPlampProjectConfig (1)` below :point_down:![`PHPlampProjectConfig 2`](<Images/PHPlampProjectConfig 2.PNG>)



- After the above has been done correctly, from the prior Ubuntu Apache2 Ubuntu default page refresh and you will see the PHP landing page.
    - see image `phpLandingPage` below :point_down:![`phpLandingPage`](Images/phpLandingPage.PNG)



