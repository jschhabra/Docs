# Install Apache2 
```
apt update 
apt install apache2
```
# Install certbot 
```
apt install software-properties-common
add-apt-repository universe
add-apt-repository ppa:certbot/certbot
apt update
apt-get install certbot python3-certbot-apache
```
# Generate certs 
```
certbot --apache -d [YOUR DOMAIN]
```
Copy paths of key and cert:
```
/etc/letsencrypt/live/[YOUR DOMAIN]/privkey.pem
/etc/letsencrypt/live/[YOUR DOMAIN]/fullchain.pem
```
We need to set them on ejabberd yml file. 