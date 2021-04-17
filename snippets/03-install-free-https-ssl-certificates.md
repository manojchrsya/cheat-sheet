#### Install Free https ssl certificates using **certbot** in apache server

```sh

sudo apt install python-certbot-apache
sudo certbot delete

sudo certbot --apache -d mydomain.com
sudo systemctl restart apache2

sudo certbot update_account --email mynewemailid.mail.com

certbot certificates

```
