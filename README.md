# Project Devops CI/CD through Jenkins

```
Requirement:
> Git install
> Jenkins
> AWS console

```

- Layout of Devops_Project

<img src="images/devopss.PNG" width=800 height=300>

# Launch the EC2 instances

- Steps to create EC2 instances:
- Choose an Amazon Machine Image (AMI):
- we recommend the Amazon Linux 2 AMI (free-tier eligible).     
Choose an instance type:
-we recommend the t2.micro (free-tier eligible).        
- Security group: you have the option to configure your virtual firewall.                           
- Launch instance: review your instance configuration and choose "Launch".       
-Create a key pair: Select "Create a new key pair" and assign a name. The key pair file (.pem) will download automatically - save this in a safe place as we will later use this file to log in to the instance. Finally, choose "Launch Instances" to complete the set up.


<img src="images/aws.PNG" width=600 height=200>


- Install Jenkins in EC2 Jenkin server:

## Steps to install Jenkins:
 First, we’ll add the repository key to the system.
- $ wget -q -O - https://pkg.jenkins.io/debian/jenkins-ci.org.key | sudo apt-key add -
- When the key is added, the system will return OK. Next, we’ll append the Debian package repository address to the server’s sources.list:
- $ echo deb https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list
- $ sudo apt-get update
- $ sudo apt-get install jenkins
- Using systemctl we’ll start Jenkins:
- $ sudo systemctl start jenkins
- $  sudo systemctl status jenkins
- If everything went well, the beginning of the output should show that the service is active and configured to start at boot:
- Output
 >  jenkins.service - LSB: Start Jenkins at boot time  
  Loaded: loaded (/etc/init.d/jenkins; bad; vendor preset: enabled)
  Active:active (exited) since Thu 2017-04-20 16:51:13 UTC; 2min 7s ago
    Docs: man:systemd-sysv-generator(8)

Opening the Firewall

- $ sudo ufw allow 8080
- $ sudo ufw status
- $ sudo ufw allow OpenSSH
- $ sudo ufw enable

To set up our installation, we’ll visit Jenkins on its default port, 8080, using the server domain name or IP address: http://ip_address_or_domain_name:8080

<img src="images/jenkins.PNG" width=700 height=300>

***

- Make new jobs


<img src="images/start.PNG" width=700 height=300>

***

-  Add the repository git

<img src="images/gitadd.PNG" width=700 height=300>

***

-  Now Build the project,search the File pom.xml

<img src="images/buildje.PNG" width=700 height=300>

***

- Build the Project

<img src="images/bulidjenk.PNG" width=700 height=200>

***

- Install Apache Tomcat in EC2 webserver

<img src="images/tomcat.PNG" width=700 height=200>

***

```
$ cat server.xml
```

Login webserver EC2 by SSH:

- check the port number of Tomcat webserver

<img src="images/port.PNG" width=700 height=300>

***
- Copy IP ip_address_or_domain_name port 8090 check Tomcat server working fine.


<img src="images/tomcat1.PNG" width=700 height=300>

***

- Add Deploy to container Plugins in Jenkins



<img src="images/addjenkins.PNG" width=700 height=300>


***

open file

```
$ cat tomcat-user.xml

```

- check the credential of webserver passwd



<img src="images/cri.PNG" width=700 height=300>

***

Add credential of jenkins

<img src="images/cridenti.PNG" width=700 height=300>

***

<img src="images/credentials.PNG" width=700 height=300>

***

<img src="images/Cr.PNG" width=700 height=300>

***

-  ADD the credential and tomcat URL:


<img src="images/addj.PNG" width=700 height=300>

***
- Build the Project, login webserver check the webapp/ dir


<img src="images/ne.PNG" width=700 height=300>

***
- ADD the cron job click in Build Triggers

<img src="images/cron.PNG" width=700 height=300>

***

- Buld the project

<img src="images/auto2.PNG" width=400 height=300>

***

- Copy the ip_address_or_domain_name browsable.


<img src="images/t.PNG" width=400 height=200>

***

- Change the code in github than again refresh the window.
  - Job automatically trigger.
  - Deployment of Webpage


<img src="images/code.PNG" width=400 height=200>

***
