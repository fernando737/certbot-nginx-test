
docker compose run --rm  certbot certonly --webroot --webroot-path /var/www/certbot/ --dry-run -d example.org  
Restart your container using docker compose restart. Nginx should now have access to the folder where Certbot creates certificates.  
However, this folder is empty right now. Re-run Certbot without the --dry-run flag to fill the folder with certificates