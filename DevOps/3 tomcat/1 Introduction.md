## Apache Tomcat
```sh
It is free and open-source.
Is a web server to run web applications, its primarily used to run java web applications.
It is lightweight and easy to set up compared to full-fledged Java EE servers like WebLogic


Note:
.Net web applications are deployed on IIS Server
Python and static web application are deployed on nginx, apache.
```
## Other webservers for Java
```sh
Oracle Weblogic
IBM Webshpere
JBoss
Pramati App Server
Sun Glassfish
```
##  illustration of SCM, Build & Tomcat
<img width="1176" height="376" alt="image" src="https://github.com/user-attachments/assets/01a0f011-86c5-4f0e-84a8-4ca5dd76661c" />

## Apache Installation and configuration
```sh
Download and install java
yum list all | grep -i java | grep corretto # java installation is mandatory 
sudo yum install java-11-amazon-corretto-devel.x86_64 # java installation is mandatory

Download apache tomcat 9x and install .
Google => Go to [http://tomcat.apache.org/download-80.cgi](https://tomcat.apache.org/download-90.cgi)and download the apache tomcat

Login to VM and go to the directory where you want to install.say /opt/bea
wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.112/bin/apache-tomcat-9.0.112.tar.gz
tar -zxvf apache-tomcat-9.0.112.tar.gz # Unzip the .tar.gz 
mv apache-tomcat-9.0.112 apache-tomcat-9 # Move the extracted folder file to a general name :
mv apache-tomcat-8.5.8 apache-tomcat
```
## Tomcat Folder structure
```sh
Tomcat deployment folder → TOMCAT_HOME/webapps
Start Tomcat → TOMCAT_HOME/bin/startup.sh
Stop Tomcat → TOMCAT_HOME/bin/shutdown.sh
Tomcat log file path → TOMCAT_HOME/logs/catalina.out
If application has issues then where do you check?
Application logs (Location is configured by application team)
```
## Modify the apache tomcat default port
```sh
TOMCAT_HOME/conf/server.xml
1. Take a back up of server.xml
    cp server.xml server.xml-def
2. Modify the port from 8080 to 8080 in server.xml
3. Restart the tomcat
    TOMCAT_HOME/bin/shutdown.sh
    TOMCAT_HOME/bin/startup.sh
```
## Tomcat Deployment Location
```sh
Deployment folder: TomcatHome}/webapps
Copy the war file to the webapp folder.
Restart the tomcat
```

    



