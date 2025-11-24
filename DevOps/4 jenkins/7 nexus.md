```sh
SSH into above ec2 instance
cd /opt
sudo wget https://download.sonatype.com/nexus/3/nexus-3.86.2-01-linux-x86_64.tar.gz
sudo tar xf nexus-3.86.2-01-linux-x86_64.tar.gz
sudo chown -R ec2-user.ec2-user nexus-3.86.2-01/ sonatype-work/
Install java
sudo yum install java-1.8.0-openjdk -y
Start nexus
/opt/nexus-3.86.2-01/bin/nexus start
Check nexus status
/opt/nexus-3.86.2-01/bin/nexus status
Open Nexus from Browser
Use 8081 as a port with public ip
Once we hit from browser, we will see prompt for login.
/opt/sonatype-work/nexus3/admin.password contains the intial password string and admin is the username
Once login, it will prompt for password change.
Disable anonymous access
```
