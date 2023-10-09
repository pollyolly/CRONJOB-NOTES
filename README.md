#### CronJob-Notes
Ubuntu
```vim
$vi /etc/crontab

# m h dom mon dow user  command
*/2 * * * *   root /bin/sh  /var/www/html/app-folder/script-file.sh >> /var/www/html/app-folder/script-file.log
```
MySQL Selecting script with Logs
```vim
$vi /app-folder/script-file.sh

#!/bin/bash
username="yourUsername"
password="yourPassword"
database="yourDatabase"
now=$(date +"%T")
mysql --user="$username" --password="$password" --database="$database" --execute="SELECT * FROM sample_table"
echo "Successfull selected all rows! Time: $now"
```
Cron Commands
```vim
crontabl -l  -check current running crontabs
service cron status/start/stop  -service of cron
```
