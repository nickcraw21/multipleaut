Ubuntu installation

1. Encrypt home directory = NO

2. Partition disc = Use Entire disc -- Write Changes = YES

3. Leave HTTP Proxy blank

4. No Automatic Updates

5. Select LAMP + OpenSSH Server with spacebar

6. Use same database password

7. Install GRUB Boot Loader = YES



In Implementatieplan volgorde commands Ubuntu Server terminal

1. sudo apt-get install phpmyadmin php-mbstring php-gettext
2. sudo apt-get install composer
3. sudo phpenmod mcrypt
4. sudo phpenmod mbstring

5. sudo apt-get install vsftpd
6. sudo nano /etc/vsftpd.conf -> haal # teken weg voor 'write_enable=YES'
7. sudo service vsftpd restart
8. zet netwerk op host-only en check ip addr show

9. Als er geen host-only is ga naar Algemene Gereedschappen

9. sudo chmod 777 /var/www/html -R

10. zet bestanden over in filezilla

11. Maak database in server 

12. cd /etc/apache2/mods-enabled/
13. sudo a2enmod rewrite -> restart apache2
14. sudo nano /etc/apache2/apache2.conf ->
find code 
	<Directory /var/www/>
	Options Indexes FollowSymLinks
	AllowOverride None <---- Verander none naar all
	Require all granted
	</Directory>

15. restart apache server -> sudo /etc/init.d/apache2 restart

16. php artisan migrate -> php artisan db:seed (nieuwe users in db)

17. Sudo apt-get install composer

18. sudo chmod 777 /var/www/html -R

19. Use Commands To Use Project
1. php artisan cache:clear
2. php artisan view:clear
3. php artisan route:clear
4. php artisan clear-compiled
5. php artisan config:cache
6. php artisan optimize --force
7. composer dumpautoload -o


16. !! Als phpymyadmin niet werkt !! -> sudo chown -R mysql:mysql /var/lib/mysql/

