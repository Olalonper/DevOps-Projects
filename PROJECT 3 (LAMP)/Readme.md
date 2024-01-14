# LAMP - Linux, Apache, MySQL, PHP or Python, or Perl

## Prerequisites;
- AWS free tier account(This has been created already).
- EC2 instance connected and running on ssh.
- Windows Powershell downloaded and connected to  instance by running the PEM key.


## Using PEM key to connect to EC2 instance via windows powershell
- ***cd download*** : This command was used to move into the into the downloads folder
- ***ssh -i lamp&lemp.pem ubuntu@x4.xx3.1xx.xx0*** : This command was used to connect the PEM key to the EC2 instance using the windows powershell. although the initial command didnt work as i had to wrap  the ampersand(&) in double quotation marks ("&") so i used this command ***ssh -i lamp"&"lemp.pem ubuntu@4.xx3.1xx.xx0***
![`EC2Running`](Images/EC2Running.PNG)
![`InstanceConnection (1)`](<Images/InstanceConnection (1).PNG>)
![`InstanceConnetion (2)`](<Images/InstanceConnection (2).PNG>)