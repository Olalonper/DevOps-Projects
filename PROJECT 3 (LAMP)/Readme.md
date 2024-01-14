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

- `SudoAptUpdate (1)` `SudoAptUpdate (2)` `SudoAptUpdate (3)` (***$ sudo apt update***) : This command was used to update a list of packages
- `SudoAptInstallApache2 (1)` `SudoAptInstallApache2 (2)` `SudoAptInstallApache2 (3)` (***$ sudo apt install apache2***) : This command was used to run apache2 package installation
- `SudoSystemctlStatusApache2` (***$ sudo systemctl status apache2***) : This command was used to verify that Apache is running using. If it is green and running that means that the apache was installed correctly.
- `CurlWebAccess (1)` `CurlWebAccess (2)` `CurlWebAccess (3)`(***$ curl http://localhost:80***) : This command was used to request the apache HTTP Server on port 80 using the DNS name and this can be pasted on your web browser to enable it display the Ubuntu Apache2 default page

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