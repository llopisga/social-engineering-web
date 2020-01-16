# social-engineering-web

This is a website made for a project on Social Engineering for the AGH University of Science and Technology whose objective is to collect only statistics for the subsequent evaluation of individuals. No passwords or other sensitive data will be stored.

## Setup instructions

1. First step - Clone website and copy all files
```
git clone https://github.com/raul-llopis/social-engineering-web.git
cd social-engineering-web
cp -r . /var/www/html
```

2. Second step - Create database and restart mysql service
```
mysql -u root
create database kapitol;
use kapitol;
create table statistics(rrss varchar(64), gender varchar (64), faculty varchar (64), free varchar (64), date varchar (64), malware varchar (64));
exit
sudo systemctl restart mysql
```

3. (Optional) Third step - Make sure the MySQL service is running
```
sudo systemctl status mysql
```

4. Fourth step - Once the test has been carried out, check db records
```
mysql -u root
use kapitol;
select * from statistics;
```
