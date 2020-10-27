# MySQL - ERROR 1298 (HY000): Unknown or incorrect time zone: 'UTC'

Let`s assume have a MySQL 5.6 Server installed on a Windows machine.
and you get the error below when trying to set time_zone to 'UTC' 
or a different time zone, follow the steps below to resolve this issue.

`SET time_zone = 'UTC';`
`ERROR 1298 (HY000): Unknown or incorrect time zone: 'UTC'`

The issue is you do not have the time zones data installed,
to install the time zones on a Windows machine, you will need:

- 1) Download "timezone_2020a_posix.zip - POSIX standard"
     from https://dev.mysql.com/downloads/timezones.html
- 2) Stop the MySQL service
- 3) Extract the files from the downloaded file 
    and copy them with overwrite
    to C:\ProgramData\MySQL\MySQL Server 5.6\data\mysql

> Yes, to C:\ProgramData\.. and not to C:\Program Files (x86)\MySQL\...

- 4) Start the MySQL service

## Fontes
- https://blog.renatolucena.net/post/como-ajustar-o-fuso-horario-ou-timezone-no-mysql
         
## O conhecimento é um tesouro, mas a prática é a chave para isso.
## Renato Lucena         
