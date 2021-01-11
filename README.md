# winsystem-whos-talking

For the WIN System: http://www.winsystem.org/.

Shows which Ham Radio nodes are keyed up at one time.

Just plop in a directory that has a PHP web server pointing at it!

## Installation

* Edit streamServer.php and add your hubs to $hubs (line 20, separated by comma)
* Change user= and group= in stream-server.service to fit your environment 
* Copy stream-server.service to /etc/systemd/system
* Make sure /srv/http/allmon2/astdb.txt exists or is a symlink to a working astdb.txt
* Make sure hideNodeURL=no in allmon.ini.php for the node stanza that's being monitored

```
./composer.phar install
systemctl enable stream-server
systemctl start stream-server
```
