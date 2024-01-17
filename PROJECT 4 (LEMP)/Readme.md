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

- ***$ sudo apt install php-fpm php-mysql*** : This command was used to install and confirm PHP components.
    - see image `installing php1` below :point_down:![`installing php1`](<Images/installing php1.PNG>)
    - see image `installing php2` below :point_down:![`installing php2`](<Images/installing php2.PNG>)
    - see image `installing php3` below :point_down:![`installing php3`](<Images/installing php3.PNG>)
    
After installing the above, refresh your browser the same browser you used to confirm if Nginx was installed correctly and you should see the PHP home page.see image `installing php3` below :point_down:![`default page for PHP`](<Images/default page for PHP.PNG>)


## Configuring Nginx to use PHP Processor
### Step 4
When using the Nginx web server, we can create server blocks (similar to virtual hosts in Apache) to encapsulate configuration details and host more than one domain on a single server. In this guide, we will use ***projectLEMP*** as an example domain name.

- ***sudo mkdir/var/www/projectLEMP*** : This command was used to create the root web directory for the domain name you want to use in this case projectLEMP is the domain nam e.
    - see image `Sudo mkdir new` below :point_down:![`sudo mkdir new`](<Images/sudo  mkdir new.PNG>)


- ***$ sudo chown -R $USER:$USER /var/www/projectLEMP*** : This command was used to assign ownership of the directory with the $USER environment variable, which will reference the current system user.
    - see image `Sudo chown new` below :point_down:![`sudo chown new`](<Images/sudo chown new.PNG>)


- ***$ sudo nano /etc/nginx/sites-available/projectLEMP*** : This command was used to open a new configuration file in Nginx's ***sites-available*** directory using your preferred command-line editor. for this we will use the nano text editor, it will create a blank file then paste the bare-bones configuration in the nano text editor.
    - see image `Sudo nano sites available` below :point_down:![`sudo nano sites available`](<Images/sudo nano sites available.PNG>)

    - see image `sudo nano bare-bone` below :point_down:![`sudo nano bare-bone`](<Images/sudo nano bare-bone.PNG>)
In the bare-bone here's what each of these directives and location blocks do:
- listen : Defines what port Nginx will listen on. In this case, it will listen on port 80, the default port for HTTP.
- root : Define the document root where the files served by this webiste are stored
- index : Defines in which order Nginx will prioritize index files for this webiste. it is a common practice to list.
- index.html : files with a higher precedence than ***index,php*** files to allow for quickly setting up a maintenance landing page in PHP applications. You can adjust these settings to better suit your application needs.
- server_name : Defines which domain names and/or IP addresses this server block should respond for. 
- location / : The first location block inclues a ***try_files*** directive, which checks for the existence of files or directories matching a URL request. If Nginx cannot find the appropriate resources, it will return a 404 error. 
- location ~ \.php$ : This location block handes the actual PHP processing by pointing Nginx to the fastcgi-php.conf configuration file and the ***php7.4-fpm.sock file***, which declares what sockket is associated with ***php-fpm***
- location ~ /\.ht : This location block deals with ***.htaccess*** files



- ***$ sudo ln -s /etc/nginx/sites-available/projectLEMP /etc/nginx/sites-enabled/*** : This command was used to activate the configuration by linking to the config file from Nginx's sites-enabled directory.
    - see image `sudo ln` below :point_down:![`sudo ln`](<Images/sudo ln.PNG>)


- ***$ sudo nginx -t*** : This command will tell Nginx to use the configuration next time it is reloaded. You can test your configuration for syntax errors .
    - see image `sudo nginx` below :point_down:![`sudo nginx`](<Images/sudo nginx.PNG>)

- ***sudo unlink /etc/nginx/sites-enabled/default*** : This command was used to disable default Nginx host that is currently configured to listen on port 80.
    - see image `sudo unlink` below :point_down:![`sudo unlink`](<Images/sudo unlink.PNG>)

- ***$ sudo systemctl reload nginx*** This command was used to reload Nginx to apply the changes made.
    - see image `sudo reload` below :point_down:![`sudo reload`](<Images/sudo reload.PNG>)