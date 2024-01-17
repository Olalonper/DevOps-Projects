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

- ***$ sudo apt install nginx*** : This command was used to run apache2 package installation.
    - see image `sudo apt install nginx1` below :point_down:![`sudo apt install nginx1`](<Images/sudo apt install nginx1.PNG>)
    - see image `sudo apt install nginx2` below :point_down:![`sudo apt install nginx2`](<Images/sudo apt install nginx2.PNG>)
    - see image `sudo apt install nginx3` below :point_down:![`sudo apt install nginx3`](<Images/sudo apt install nginx3.PNG>)



- ***$ sudo systemctl status apache2*** : This command was used to verify that Apache is running using. If it is green and running that means that the apache was installed correctly.
    - see image `sudo systemctl status nginx` below :point_down:![`sudo systemctl status nginx`](<Images/sudo systemctl status nginx.PNG>)
    
    
- ***$ curl http://localhost:80*** : The ***curl*** command when run will return strangely formatted texts basically a bunch of html codes, but not cause for alarm its just to make sure that the Nginx web service responds to ***curl*** command with some payload.
    - see image `CurlWebAccess (3)` below :point_down:![`CurlWebAccess (3)`](<Images/CurlWebAccess (3).PNG>)

- OR you can copy the IP address and paste it on your browser to confim that Nginx works correctly. either you do the above or below you should get the below in your web browser.
    - see image `testing nginx server from the web browser` below :point_down:![`testing nginx server from the web browser`](<Images/testing nginx server from the web browser.PNG>)



