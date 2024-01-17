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
    - see image `MySQLSecureInstallationWithPASSWORDchange` below :point_down:![`sudo mysql secure installation1`](<Images/sudo mysql secure installation1.PNG>)
    - see image `MySQLSecureInstallationWithPASSWORDchange` below :point_down:![`sudo mysql secure installation2`](<Images/sudo mysql secure installation2.PNG>)

- ***$ sudo mysql -p*** : This command was used to test if one is able to log into the MySQL console, -p flag in this command will prompt you for the password used after changing the root user password and to exit the MySQL console for this you will use the password you created in the above step, type ***mysql> exit***.
    - see image `sudo mysql -p` below :point_down:![`sudo mysql -p`](<Images/sudo mysql -p.PNG>)


