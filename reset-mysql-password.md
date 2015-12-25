# Reset mysql password

[Ref](https://help.ubuntu.com/community/MysqlPasswordReset)

```
sudo /etc/init.d/mysql stop
sudo /usr/sbin/mysqld --skip-grant-tables --skip-networking &
mysql -u root
FLUSH PRIVILEGES;
SET PASSWORD FOR root@'localhost' = PASSWORD('password');
UPDATE mysql.user SET Password=PASSWORD('newpwd') WHERE User='root';
```

purge

```
sudo apt-get --purge remove mysql-server mysql-common mysql-client
sudo apt-get install mysql-server mysql-common mysql-client
mysqladmin -u root password your-new-password
sudo /etc/init.d/mysql restart
mysql -u root -p
```

easiest method

```
sudo dpkg-reconfigure mysql-server-N.N #N.N is the MySql Server version
```
