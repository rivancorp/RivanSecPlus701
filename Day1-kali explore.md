### task1: make sure xammp is running

sudo /opt/lampp/lampp start  --> 
sudo systemctl stop apache2

http://127.0.0.1/mutillidae/src/index.php

http://208.8.8.133/mutillidae/src/index.php

if you want mutillidae to be accessed via web:
sudo nano /opt/lampp/htdocs/mutillidae/.htaccess

Order Deny,Allow
Deny from all
Allow from 127.0.0.1
Allow from ::1
Allow from 192.168.0.0/16
Allow from 10.0.0.0/8
Allow from 172.16.0.0/12
Order Allow,Deny
Allow from all

sudo rm /opt/lampp/htdocs/mutillidae/.htaccess
sudo /opt/lampp/lampp restart

### task2: open the web: SQL INJECTION:

![image](https://github.com/user-attachments/assets/b565d468-aa2d-4c6d-99b0-d78910e672fb)

create a user name: anne curtis with password C1sc0123

![image](https://github.com/user-attachments/assets/ac571ec9-1f25-4b07-954e-b5b8ce838b7f)

' OR 1=1 -- -
' OR 1=1 -- -
