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



