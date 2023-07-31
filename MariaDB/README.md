### Authentication
#### Unix Socket
A new MariaDB installaion will have two all-powerful accounts -root and the OS user that owns the data directory, typically mysql.
They are created as
```
CREATE USER root@localhost IDENTIFIED VIA unix_socket
CREATE USER mysql@localhost IDENTIFIED VIA unix_socket
```
Using unix_socket means that if you are the system root user, you can login as root@locahost without a password. It is based on a simple fact, that asking the system root for a password adds no extra security — root has full access to all the data files and all process memory anyway. But not asking for a password means, there is no root password to forget. And if you want to script some tedious database work, there is no need to store the root password in plain text for the scipt to use.
