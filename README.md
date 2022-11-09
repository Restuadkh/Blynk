# Blynk
cd /var/www/html/
wget 

# Run
java -jar ./blynk-server.jar -dataFolder ./Blynk  

# job Reboot to StartUp
crontab -e

@reboot java -jar /var/www/html/blynk-server.jar -dataFolder /var/www/html//Blynk 