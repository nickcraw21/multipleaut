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

9. zet bestanden over in filezilla
10. sudo chmod 777 /var/www/html -R

11. cd /etc/apache2/mods-enabled/
12. sudo a2enmod rewrite -> restart apache2
13. sudo nano /etc/apache2/apache2.conf ->
find code 
	<Directory /var/www/>
	Options Indexes FollowSymLinks
	AllowOverride None <---- Verander none naar all
	Require all granted
	</Directory>

14. restart apache server -> sudo /etc/init.d/apache2 restart

15. php artisan migrate -> php artisan db:seed (nieuwe users in db)



16. !! Als phpymyadmin niet werkt !! -> sudo chown -R mysql:mysql /var/lib/mysql/

