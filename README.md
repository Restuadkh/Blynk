# Blynk

cd /var/www/html/

- ubuntu

apt-get install wget

- centos / redhat

yum install wget

wget https://github.com/Restuadkh/Blynk/blob/master/blynk-server.jar

# open firewall
- ubuntu

iptables -A INPUT -p tcp --dport 9443 -j ACCEPT

iptables -A INPUT -p tcp --dport 8080 -j ACCEPT


- centos / redhad

firewall-cmd --permanent --zone=public --add-port=8080/tcp

firewall-cmd --permanent --zone=public --add-port=9443/tcp

# Run
java -jar ./blynk-server.jar -dataFolder ./Blynk  

login to localhost:9443

Set Email field to 'admin@blynk.cc'

Set password field to 'admin'

Click Login

# job Reboot to StartUp

crontab -e

@reboot java -jar /var/www/html/blynk-server.jar -dataFolder /var/www/html//Blynk 

# App Blynk APk

https://github.com/Restuadkh/Blynk/blob/master/Blynk.apk

Install Apps

Switch server from BLYNK to CUSTOMS

Set your local blynk server IP

Set port to 8080 or 9443

click OK