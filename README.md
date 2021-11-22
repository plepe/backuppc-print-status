Print status of each backup host

INSTALL
```sh
apt install php-cli libjson-xs-perl git
cd /usr/local
git clone https://github.com/plepe/backuppc-print-status
cd backuppc-print-status
cp conf.php-dist conf.php
nano conf.php
```

Add this to `/etc/crontab`:
```
0 9	* * * 	backuppc /usr/local/backuppc-print-status/backuppc-print-status 2> /dev/null
```
