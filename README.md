# Blynk

cd /var/www/html/

- ubuntu

apt-get install wget

- centos / redhat

yum install wget

wget https://github.com/Restuadkh/Blynk/blob/master/blynk-server.jar

# add user Blynk

cd /var/www/html/Blynk/

cp admin@blynk.cc.Blynk.user user@blynk.cc.Blynk.user

nano user@blynk.cc.Blynk.user

- Editor

{
"name":"user@blynk.cc",

"email":"user@blynk.cc",

"appName":"Blynk",

"region":"local",

"ip":"127.0.0.1", # ip first instal

"pass":"00zAZN1ejHfoXi758jhbb1UPdrPCMvRptsfiXOcuJ/c=", # can change to login > admin@blynk on web view

"lastModifiedTs":1667952258536,  # auto update for edit user

"lastLoggedIP":"192.168.1.10", # last login for

"lastLoggedAt":1667924549057, # auto update for login

"profile":{

        "pinsStorage":{"882220015-0-v5":"22"}},

        "isFacebookUser":false,

        "isSuperAdmin":true,

        "energy":100000, # can change for your fun

        "id":"user@blynk.cc-Blynk"}
		

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

# Library for Arduino

https://github.com/Restuadkh/Blynk/blob/master/Blynk_Release_v1.1.0.zip

Instal to arduino

Skath -> Include Library -> add .ZIP Library