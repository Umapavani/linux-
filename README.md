Udacity-Linux-Server-Configuration
By Umapavani
About
This is the Udacity project 5 about the Configuring the Linux the server.

Server Details
Server IP Address 13.127.109.112

Hosted site Url http://13.127.109.112.xip.io/

How to connect as grader:
save private key provided in your local machine and run the following command

ssh -i path/to/privatekey -p 2200 grader@13.127.109.112
  
Configuring Linux Server
Updating all packages
sudo apt-get update
sudo apt-get upgrade
Creating grader User:
sudo adduser grader
This will add new user

sudo nano /etc/sudoers
Below the Root user append the following line

grader  ALL=(ALL:ALL) ALL
This will grant sudo permission to grader

Creating a ssh key pair for grader
On your local machine in terminal/command prompt

ssh-keygen
This will generate public and private ssh keys which is saved to .ssh folder
#id_rsa:
-----BEGIN RSA PRIVATE KEY-----
MIIEpAIBAAKCAQEA4KgEHTkQPyAatTy/m09Um7v2BlNuiduW7gvXwglAdYauuEiy
j0oea7plXoFGtbBn4EaQMRdUiYQC7nTx6qRlznRtSAuEDq3/CKZJhms7HAvgIRXA
epKW73zq83BvahRHN0R3jy6jyaT4w8rth06reJYUM/5oyaLf9+1JdnFEPzeJ3wKE
D5+5Vq7eZridAUG9ZwYxxvs75a2VDxPmGKUrToGSM2E/fe4sLoX0ptp9qfGqiqyF
aQ8ZojI+5ZPFjYa9k2Zp7SAMea9HE770WpaG/1fs4NEyTOyLvFFjZ/0VZwlcihCA
nuy2N7H6hjsMHwHn9+tebJVr3XtIn7poX8CKEwIDAQABAoIBAQC56RCOhlx1gMHZ
XY5KnlmsDt3H2l9NYhUCpXZFMpbPK0eHZVGu1m1aRQQCMwUq8fLkXECS/3WL31z1
rH1N6gH92cddqXn9E+xLYiDSRgbCbOlrN67zQD/7q+pazp7EsEdG6zftm3EbO5RJ
orLyGB46Sigp5s0cn9asOwdiJtWNYYDJReGSlJqS8c9fNhrFZdukevLO+Lq4YLlM
R0rlMxR9xWCdP2kkPCiAt/pwJPjHjoGqfr9Qb5HSYCAsA5AOEj3t4ZqSUXYYw1mj
5pi8YILFdaOmD6YvIWXVFXU8qx3eyUGouyeA+82sFQMFDq+yDGWSq2RSpi/0ixdV
D0Q+8DiRAoGBAP/8heErUR9ko1TOZEJmANuNhxUzvdYk6f6xloqFLG7OTOecUYwD
OfsZHIxMAHMSZloORaea8j2bYDMRxziILDU3f3fQyAQYnbnuba9C/qJjqnXcUG8c
H7ZCIZVWchNz7rEsWdf9Hevi8gKdKHJiRGh+hdN733okaKDFouHycvkfAoGBAOCr
EUsB4i4sjlD0yv5iRGYNxCT6RsOT3gXCXAIRUvJ6XNWNGfYOT36/QTuHzRM6Q+ja
IDk41/rXRyw8dV3qB/5k1cpDLqcaOqdYziMofG80jmjeGh+XXU7Qj9embbhtScaX
vamakfPEKg5tBmGBeMz57OzgZ4mUni2wsTFM5CyNAoGBAOiL7tNvFnL+aaJRHKN1
JrJND7ojFwHC5w+JJMkR0huXLiX5y9r102ZYmaaaJI5k2LZW4NAx4n40+F9sdx7U
FdUCZbni4NFXy3FtOBdPNSMwh1oqmqdVVTmtOfUAYwFpAB3TvIqKVvRDZrcZLfU7
cAm9ZrWIgqvjB2mGIUJBjlDhAoGAI5j3VHsn60kEA6/Fuii3zbPAsFs3eyWiuCbj
jTBRhDn/G5cP1fzOe7ayD0ylIbbJq8tj760iC4ywqkGqFwdN3PD9Lt8WNUPip0Fa
6BcyICyjo9oNKZRCJIrHP9QO7nnihqTkWEs1dPpP75k2uZxaF6BB+gZUYWg65+Jn
MPiN7sECgYAWOze5No9v0M3f5GEQPAemDe1/cQXXFfj39+PUJOB72+5WSLwwLMKM
L53XGsaWJfxYEHYwGVHINPqI8/Yj/9Kud77K6c9S63bfmdx1MEP8EDZ1pVKpNB68
U6k9Ie1os6WOXz8ELhw8dK266Iq8NzXy+ZDLLl6a92SQ2nH0z0HYzA==
-----END RSA PRIVATE KEY-----
#id_rsa.pub:
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDgqAQdORA/IBq1PL+bT1Sbu/YGU26J25buC9fCCUB1hq64SLKPSh5rumVegUa1sGfgRpAxF1SJhALudPHqpGXOdG1IC4QOrf8IpkmGazscC+AhFcB6kpbvfOrzcG9qFEc3RHePLqPJpPjDyu2HTqt4lhQz/mjJot/37Ul2cUQ/N4nfAoQPn7lWrt5muJ0BQb1nBjHG+zvlrZUPE+YYpStOgZIzYT997iwuhfSm2n2p8aqKrIVpDxmiMj7lk8WNhr2TZmntIAx5r0cTvvRalob/V+zg0TJM7Iu8UWNn/RVnCVyKEICe7LY3sfqGOwwfAef3615slWvde0ifumhfwIoT hp@DESKTOP-E82NM60
#ptest.pem:
-----BEGIN RSA PRIVATE KEY-----
MIIEoAIBAAKCAQEAxEfgRNDc8r0Qjg0vxQDlhnl+LnLUBJc5uO/CIqpGQ5kZijzE
4r3pLfFD5wTG5kZbNM8dDxu6g994xNpy4tplhSO4j6h2EoBYutcxF5MTTZWJ3c/x
Px5avcN5iwnNe4FgA9nflbVWZCTY4puaZR/N7lwkufXT5/kVTRmpZ0NKsaPJ2wRE
eHKYw93KJNKExDcYmTDXSomJVdi/TR8Az3iDlf2tdpxLEOeEqJ39zZmLpxd2rji1
1G4nGfFRaqZwBDu6mnaNdOs0VU9uVwRIifhFSf2bT1/Ofe2ykrRjbeKMNFeWf75T
lSz07z/iQqzHoq10/Jjt/0T57zkFE2p7wRmZuQIDAQABAoIBABcmqysyv3zaFAPN
Rl8kNe5gkiOEY8GO3L4VeX6BOvxqKHsHo+lioQhMNsge5h7vGX7nFvRbPuqjBymg
4oAjZmoHxpMbOaIBBXY0P5QaQuKZysMg7cGWIPnU/pcJtvTkU6Dgp+COnPv+5J4F
4HYhBDcjIynT9wSbeom3hyWo6Dx/cj2UIMdzddjWza/sdp2Cx3fPEVeJkH0iPTNc
dfJl3xR9HGEfXnH3MlkwgIdy3WsYSummRJVkN5NKwKN8auD+SmJI5fBQxXsA4imO
2ly+r6Vx+i3EhZ418EhrFwClHb4lN5K7gdSQVRWyaIpBHSt0xUtaDwquOpESqviG
d0fX0gECgYEA52wVVdCp7C+oaMGj/VwasACveiHrNgI9WWsn23IfTXiL7VK+drsz
bhmZBQHV5eUtoWLkMJ16Pjxo2N0fOuOTXGiBLsMiqyWaO6Sc5E2ivMFlY6jZHk76
QgoaVRtvJ+5+JETHJbrY8bjgERhxbcCoyYp75AScOzuKmkvZhFHtHlkCgYEA2SBd
qoNYsXhvL8DEd9ea87ym8pDX0Sab6rKvPLeiJ2YZKj3W0qJ7ckgvgRwxs7wHLNwD
+GjNMjRKaRyxt/ZLZN2qHnjdE1xnmQQa03VT/zkf4Um1AdPTXYMgANGebpBVHfsD
Nx+a5WfNfr8CE5aT+nXpB/ez5bzY32FzKsGqqmECgYByET1G6i4HQ8pfsCqTpEVn
QT89FODp4xq4K3Ae41Z4ihV2adWFkmocN7PL2wbCZT8jkCnnqIdri70mP3+4OBoX
b09VbEt3TnaCNXY7teSj4zOFduFl5gnGaVJnZrlYVl6Io/oBJ+Ls6nJPGtw1+8N2
a7L7RiZ3r7Z2rTJO3U7iKQJ/Scm2CzyX57gGETRxkEi1YB+8nLKcpXd5hUk0RG4j
rUAFTVW2q96MFUpy2m26dlpwFc6virwS//zFTPNzchFBjgXGypRIjUvZ6SZ792Do
KtQ/AVELMpPKQP1O4vhZ3zkttAKaFSGogk3EiE5hZkbGA1gO2aZUfL6w9Tko6l7m
oQKBgE/3KnCh1bsqOutx8ksCVU4jz8DRG7uGbIfclXrtoW1a4C8ekvy2Li9VqCfL
yUbCOiT81Iq8fe3gk2ws0bUz1YqdVz0TqmKhXV5J8SuOXIg0BQ3hwvQ1QgRs0Uyr
QvIOjPto9utqX86ntPvHxPxMrs9e09uitIZiBM7rzUPeiSRk
-----END RSA PRIVATE KEY-----

#privatekey is saved as privatkey1.ppk:
PuTTY-User-Key-File-2: ssh-rsa
Encryption: none
Comment: imported-openssh-key
Public-Lines: 6
AAAAB3NzaC1yc2EAAAADAQABAAABAQDER+BE0NzyvRCODS/FAOWGeX4uctQElzm4
78IiqkZDmRmKPMTivekt8UPnBMbmRls0zx0PG7qD33jE2nLi2mWFI7iPqHYSgFi6
1zEXkxNNlYndz/E/Hlq9w3mLCc17gWAD2d+VtVZkJNjim5plH83uXCS59dPn+RVN
GalnQ0qxo8nbBER4cpjD3cok0oTENxiZMNdKiYlV2L9NHwDPeIOV/a12nEsQ54So
nf3NmYunF3auOLXUbicZ8VFqpnAEO7qado106zRVT25XBEiJ+EVJ/ZtPX8597bKS
tGNt4ow0V5Z/vlOVLPTvP+JCrMeirXT8mO3/RPnvOQUTanvBGZm5
Private-Lines: 14
AAABABcmqysyv3zaFAPNRl8kNe5gkiOEY8GO3L4VeX6BOvxqKHsHo+lioQhMNsge
5h7vGX7nFvRbPuqjBymg4oAjZmoHxpMbOaIBBXY0P5QaQuKZysMg7cGWIPnU/pcJ
tvTkU6Dgp+COnPv+5J4F4HYhBDcjIynT9wSbeom3hyWo6Dx/cj2UIMdzddjWza/s
dp2Cx3fPEVeJkH0iPTNcdfJl3xR9HGEfXnH3MlkwgIdy3WsYSummRJVkN5NKwKN8
auD+SmJI5fBQxXsA4imO2ly+r6Vx+i3EhZ418EhrFwClHb4lN5K7gdSQVRWyaIpB
HSt0xUtaDwquOpESqviGd0fX0gEAAACBAOdsFVXQqewvqGjBo/1cGrAAr3oh6zYC
PVlrJ9tyH014i+1Svna7M24ZmQUB1eXlLaFi5DCdej48aNjdHzrjk1xogS7DIqsl
mjuknORNorzBZWOo2R5O+kIKGlUbbyfufiRExyW62PG44BEYcW3AqMmKe+QEnDs7
ippL2YRR7R5ZAAAAgQDZIF2qg1ixeG8vwMR315rzvKbykNfRJpvqsq88t6InZhkq
PdbSontySC+BHDGzvAcs3AP4aM0yNEppHLG39ktk3aoeeN0TXGeZBBrTdVP/OR/h
SbUB09NdgyAA0Z5ukFUd+wM3H5rlZ81+vwITlpP6dekH97PlvNjfYXMqwaqqYQAA
AIBP9ypwodW7KjrrcfJLAlVOI8/A0Ru7hmyH3JV67aFtWuAvHpL8ti4vVagny8lG
wjok/NSKvH3t4JNsLNG1M9WKnVc9E6pioV1eSfErjlyINAUN4cL0NUIEbNFMq0Ly
Doz7aPbral/Op7T7x8T8TK7PXtPborSGYgTO681D3okkZA==
Private-MAC: 94ac87719053f82157d1d186ecb4f0430051071c


Then in your virtual machine change to newly created user

su - grader
Create a new directory .ssh and new file authorized_keys in that directory

mkdir .ssh
sudo nano .ssh/authorized_keys
Copy the public key with .pub extension to authorized_keys and save the file

chmod 700 .ssh
chmod 644 .ssh/authorized_keys
700 will give read write and execute permission to user.
644 prevent other user from writting in to file. Then restart ssh server
service ssh restart
Now from your log in to grader with private key generated

ssh -i .ssh/id_rsa grader@13.127.109.112 
Changing the ssh port to 2200
sudo nano /etc/ssh/sshd_config
Change port 22 to port 2200

Restart the ssh server

service ssh restart
Note: Before Logging using ssh add custom TCP port 2200 under lightsaail firewall in networking tab in lightsail instance console

Now Login using command like this

ssh -i .ssh/id_rsa -p 2200 grader@13.127.109.112
Disabling ssh login as root
sudo nano /etc/ssh/sshd_config

make change PermitRootLogin no

Configurating Ufw firewall
sudo ufw allow 2200/tcp
sudo ufw allow 80/tcp
sudo ufw allow 123/udp
sudo ufw enable
This will allow all required ports and enables the ufw

After that

sudo ufw status
It will display all allowed ports

Changing time Zone
sudo dpkg-reconfigure tzdata

select none from list and then select utc.

Installing Apache2
In terminal

sudo apt-get install apache2

Now mod_wsgi

sudo apt-get install python-setuptools libapache2-mod-wsgi

Enable mod_wsgi

sudo a2enmod wsgi

Setting up your flask application to work with apache2
Creating a flask app

In /var/www directory create a new folder sudo mkdir FlaskApp

Install git

sudo apt-get install git

move to the FlaskApp cd FlaskApp

In that direcory clone your github repository

sudo git clone https://github.com/Umapavani/catalog.git

Rename your repository to FlaskApp

Then rename your project file to __init__.py

Error : While accesssing the client_secrets.json file

PROJECT_ROOT = os.path.realpath(os.path.dirname(__file__))
json_url = os.path.join(PROJECT_ROOT, 'client_secrets.json')
CLIENT_ID = json.load(open(json_url))['web']['client_id']
Use json_url instead client_secrets.json in script

Reffered from stack overflow

Install and configuring postgresql for project
Install Postgres sudo apt-get install postgresql

login to postgres sudo su - postgres

postgres shell psql

create user CREATE USER catalog WITH PASSWORD 'password';

permit user to createdb ALTER USER catalog CREATEDB;

Create a db name catalog with user catalog CREATE DATABASE catalog WITH OWNER catalog;

connect to db \c catalog

revoke all permission to public REVOKE ALL ON SCHEMA public FROM public;

Give schema permission to user catalog GRANT ALL ON SCHEMA public TO catalog;

exit from db and postgres \q and exit

Change the database connection in both db_setup.py and __init__.py as engine = create_engine('postgresql://catalog:password@localhost/catalog')

Now you are ready with your applicatiom

Configure and Enable a New Virtual Host
sudo nano /etc/apache2/sites-available/FlaskApp.conf

In this add the following code

<VirtualHost *:80>
 	ServerName 13.127.109.112
 	ServerAdmin admin@13.127.109.112
 	WSGIScriptAlias / /var/www/FlaskApp/flaskapp.wsgi
 	<Directory /var/www/FlaskApp/FlaskApp/>
 		Order allow,deny
 		Allow from all
 	</Directory>
 	Alias /static /var/www/FlaskApp/FlaskApp/static
 	<Directory /var/www/FlaskApp/FlaskApp/static/>
 		Order allow,deny
 		Allow from all
 	</Directory>
 	ErrorLog ${APACHE_LOG_DIR}/error.log
 	LogLevel warn
 	CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
Enable the virtual host sudo a2ensite FlaskApp

Disabling the default apache2 page sudo a2dissite 000-default.conf

Create the .wsgi File
```
cd /var/www/FlaskApp
sudo nano flaskapp.wsgi 
```
Add the following code

#!/usr/bin/python
 import sys
 import logging
 logging.basicConfig(stream=sys.stderr)
 sys.path.insert(0,"/var/www/FlaskApp/")

 from FlaskApp import app as application
 application.secret_key = 'Add your secret key'
save and exit

Deploying flask app with apache2 is referred from Digital ocean

Installing require modules
You can either install all modules on your machine or create a virtual environment for the project and install the modules pip install flask sqlalchemy psycopg2 requests oauth2client

Setting up your Google Oauth2
Login to your developer console and select your project and edit OAuth details as following

Javascript origin http://ip.xip.io

redirect URI

http://ip.xip.io\login

http://ip.xip.io\gconnect

http://ip.xip.io\callback

xip.io is a free DNS which will be the same as using IP address

Final Step
Restart your apache2 server

sudo service apache2 restart
