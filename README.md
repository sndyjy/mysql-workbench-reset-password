# mysql-workbench-reset-password

Found this on stock overflow. This will be helpful when mysql password was forgotten.


## This is based on this helpful Video on Youtube:
https://www.youtube.com/watch?v=V8_fpBE9deA&ab_channel=CSCORNERSunitaRai


## Solution in summary:

### Press **win + R**

type ``` services.msc ```


### Stop *MySQL80* service


### Create a text file named *mysql-init.txt* in the root of C drive or in any desired location:

e.g: ``` C:\mysql-init.txt ```


### Add the following content to *mysql-init.txt*

```ALTER USER 'root'@'localhost' IDENTIFIED BY 'new_password_here';```

 
### Last Step: Open CMD with Admin rights:


### Navigate to "C:\Program Files\MySQL\MySQL Server 8.0\bin" in CMD

*C:\Windows\system32>* ```cd C:\Program Files\MySQL\MySQL Server 8.0\bin```


### Then Type in the command : 
(Take note that the last part of the command *C:\Users\wow\Desktop\mysql-init.txt* is the location of the file created earlier)

```mysqld --defaults-file="C:\ProgramData\MySQL\MySQL Server 8.0\my.ini" --init-file="C:\Users\wow\Desktop\mysql-init.txt"```

e.g:

*C:\Program Files\MySQL\MySQL Server 8.0\bin>* ```mysqld --defaults-file="C:\ProgramData\MySQL\MySQL Server 8.0\my.ini" --init-file="C:\mysql-init.txt" --console```

### Do not close the CMD window

### Try connecting to  MySQL server before restarting "MySQL80" service

### Search and open in windows Searchbar *MySQL 8.0 Command Line Client*

## Enter the newly created password to check if it worked or not

It should work, If not then just watch the Youtube Video above.
