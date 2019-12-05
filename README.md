## 999_Configure_Apache

This files is for apache2 on the following setting.  
 1. Raspbian at Raspberry Pi3
 1. Enable cgi of python3
 1. Python run at "/media/pi/myUSB/011_yt_cast/rasUSB/cgi-bin/" on USB memory
 1. don't install mod_wsgi


***
apach2 option

pi@raspberrypi:~ $ apache2ctl configtest  
AH00558: apache2: Could not reliably determine the server's fully qualified domain name, using 127.0.1.1. Set the 'ServerName' directive globally to suppress this message  
Syntax OK  

pi@raspberrypi:~ $ apache2ctl -t -D DUMP_VHOSTS  
AH00558: apache2: Could not reliably determine the server's fully qualified domain name, using 127.0.1.1. Set the 'ServerName' directive globally to suppress this message  
VirtualHost configuration:  
*:80                   127.0.1.1 (/etc/apache2/sites-enabled/000-default.conf:1)  
*:8080                 127.0.1.1 (/etc/apache2/sites-enabled/000-default.conf:32)  

pi@raspberrypi:~ $ apache2ctl -t -D DUMP_VHOSTS -D DUMP_RUN_CFG  
AH00558: apache2: Could not reliably determine the server's fully qualified domain name, using 127.0.1.1. Set the 'ServerName' directive globally to suppress this message  
VirtualHost configuration:  
*:80                   127.0.1.1 (/etc/apache2/sites-enabled/000-default.conf:1)  
*:8080                 127.0.1.1 (/etc/apache2/sites-enabled/000-default.conf:32)  
ServerRoot: "/etc/apache2"  
Main DocumentRoot: "/var/www/html"  
Main ErrorLog: "/var/log/apache2/error.log"  
Mutex watchdog-callback: using_defaults  
Mutex default: dir="/var/run/apache2/" mechanism=default   
PidFile: "/var/run/apache2/apache2.pid"  
Define: DUMP_VHOSTS  
Define: DUMP_RUN_CFG  
Define: ENABLE_USR_LIB_CGI_BIN  
User: name="www-data" id=33 not_used  
Group: name="www-data" id=33 not_used  

***
#Referenced URL (Japanese only)
- https://qiita.com/aryoa/items/2c28b466e911a3dd101d  
- https://qiita.com/takey/items/75e6984468f0f6870a97  
- https://qiita.com/ninneko/items/87a76f0f1dc6d82500fb  
- https://www.itmedia.co.jp/help/tips/linux/l0264.html  
- https://www.itmedia.co.jp/help/tips/linux/l0237.html
- https://qiita.com/lamplus/items/9877849d3108e2c6d0df
