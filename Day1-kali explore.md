
**Markdown:**

```markdown
# Heading 1  
## Heading 2  
### Heading 3
```


### task1: make sure xammp is running
```
sudo /opt/lampp/lampp start  --> 
sudo systemctl stop apache2
```
http://127.0.0.1/mutillidae/src/index.php

http://208.8.8.133/mutillidae/src/index.php

if you want mutillidae to be accessed via web:
sudo nano /opt/lampp/htdocs/mutillidae/.htaccess
```
Order Deny,Allow
Deny from all
Allow from 127.0.0.1
Allow from ::1
Allow from 192.168.0.0/16
Allow from 10.0.0.0/8
Allow from 172.16.0.0/12
Order Allow,Deny
Allow from all
```

sudo rm /opt/lampp/htdocs/mutillidae/.htaccess
sudo /opt/lampp/lampp restart

### task2: open the web: SQL INJECTION:
```

SQL Injection is a web security vulnerability that allows an attacker to interfere with the queries an application makes to its database.
By injecting malicious SQL code into input fields (like login forms or search boxes), attackers can:
Bypass authentication
View, modify, or delete data
Execute administrative operations
Extract sensitive information

```
![image](https://github.com/user-attachments/assets/b565d468-aa2d-4c6d-99b0-d78910e672fb)

create a user name: anne curtis with password C1sc0123

![image](https://github.com/user-attachments/assets/ac571ec9-1f25-4b07-954e-b5b8ce838b7f)

If a website runs this code:

```
SELECT * FROM users WHERE username = 'input' AND password = 'input';

```
An attacker could input:
```
' OR 1=1 -- -
' OR 1=1 -- -

' OR '1'='1
' OR '1'='1

```
![image](https://github.com/user-attachments/assets/829dc8d0-98c4-43cc-af92-634b35148679)

and type: ' OR 1=1 -- - or both user and password:

![image](https://github.com/user-attachments/assets/271fc5d4-0532-4362-bda0-ab200f342fc9)

### we get this:

![image](https://github.com/user-attachments/assets/8eef2ed0-ecff-4391-8b9f-39e1bf2dee29)

## TASK2:A4: XML External Entities (XXE)

Go to: OWASP 2017 → A4 - XML External Entities

![image](https://github.com/user-attachments/assets/0b7fcd66-3965-4403-9a9a-6642d8ef6f15)

Paste this payload:
```

<?xml version="1.0" encoding="ISO-8859-1"?>
<!DOCTYPE foo [  
  <!ELEMENT foo ANY >
  <!ENTITY xxe SYSTEM "file:///etc/passwd" >]>
<foo>&xxe;</foo>

```
![image](https://github.com/user-attachments/assets/a1bfdd93-cfd8-4390-a101-8f1c7d8237e4)

You get contents of a password file:

![image](https://github.com/user-attachments/assets/61e65d11-0f36-4161-9a7f-a25849f302ba)

## TASK2:A4: Honey Pot demo:

```

cd /home/kali/pentbox-1.8
 ./pentbox.rb

```

![image](https://github.com/user-attachments/assets/6ad8f047-1b6f-46bc-a8e3-a7af507e5829)

we shall make a fake smtp port 25 to have hackers to connect to it: first nmap your kali linux:

![image](https://github.com/user-attachments/assets/7f4824f4-a5d5-4728-84d6-b10b6cb8cccb)

now type: 2  then 3  then 2  then 25  then "this is mail server" then n  then n

![image](https://github.com/user-attachments/assets/c36dbc69-1842-4b2c-ac86-249c38783912)

Now nmap from windows and see if port 25 is open and try to telnet 25:

![image](https://github.com/user-attachments/assets/1db8343e-3b23-49ea-9fae-052f289f6efd)

Now check the kali console:

![image](https://github.com/user-attachments/assets/200a0236-a313-418b-9ddb-8b7d24cc5323)

Now do this for port 23:


## TASK2:A4: XML External Entities (XXE)
