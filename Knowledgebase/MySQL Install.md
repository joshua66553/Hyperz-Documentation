This guide will explain how to INSTALL MySQL on different OS's

---

# AVAILABLE OS's

- [Windows 10](#windows)
- [Linux Ubuntu 20](#linux-ubuntu)

---

# Windows

#### Required Programs:

- [XAMPP](https://www.apachefriends.org/index.html)
- [HeidiSQL](https://www.heidisql.com/download.php)

---

#### XAMPP:

- Go through the installer for XAMPP as you normally would.
- When complete, click the checkbox here: ![](https://cdn.hyperz.net/2cpf6k6i.png)
- Then click the small start buttone here: ![](https://cdn.hyperz.net/zkwq2511.png)

This should get the program to start using MySQL, and it should start console logging something like the below screenshot:

![](https://cdn.hyperz.net/mfngpqdl.png)

---

### HeidiSQL:

- First thing is to open HeidiSQL.
- It may look like this:
![](https://dev.Jipythedev.xyz/image/heidisql_sXP7QnByqO.png)
- So put hit new then put a name or something.
- The login details may be the same like this:
`Hostname/IP  = localhost, 
Username       = root, 
Password        = <Nothing>, 
Port                  = 3306`
- Once the details have been entered then hit open.
- It may look like this:
![](https://dev.Jipythedev.xyz/image/heidisql_i3iUUxODuc.png)
- Right click on this bit:
![](https://dev.Jipythedev.xyz/image/heidisql_TwodsckzQu.png)
- Then hit Create New then click Database like this:
![](https://dev.Jipythedev.xyz/image/heidisql_pp2M1sGYY9.png)
- In the box put a database name you prefer then click ok:
![](https://dev.Jipythedev.xyz/image/heidisql_kgRJiUMuX9.png)
- Once the database has been made click files at the top left.
- Then hit load sql file or press `CTR + O`and choose all the sql files you need to execute.
- Then it should look like this:
![](https://dev.Jipythedev.xyz/image/heidisql_HfbdwTK0zJ.png)
- Then press the blue play button it looks like this:
![](https://dev.Jipythedev.xyz/image/heidisql_Ad97r44PlV.png)
- This will load all the tables and make then in your database.
- Once you have done that then the database is all set and then you can setup the **config** file and put all the MySQL details in.


---

# Linux Ubuntu

Start off by running this command to install the base of MySQL:
`sudo apt install mysql-server`

When prompted press `Y` to install MySQL-Server.

Then lets install the secure installation below:
`sudo mysql_secure_installation`

It will likely ask you if you wish to remove things, press `Y` for **most** of these.

---

#### Changing your MySQL Password in Linux Ubuntu

- Run `mysql -u root -p`
- Enter your current password
- Enter the following commands

```
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'SETYOURPASSWORDHERE';
FLUSH PRIVILEGES;
```

- Then your password will be changed!

---

#### Create A MySQL Database

- Run `mysql -u root -p`
- Enter your current password
- Enter the following command: `CREATE DATABASE databasenamehere;`
- Then you have made a MySQL Database

---

#### Import an SQL File

- Run `mysql -u root -p`
- Enter your current password
- Make sure you already have a database created
- Enter the following commands

```
use databasename;
source /path/to/your/file.sql
```

- To check that all the tables have been imported, run: `SHOW TABLES;`
- Then you're done!

---
