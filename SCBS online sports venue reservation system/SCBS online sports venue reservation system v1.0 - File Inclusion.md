# SCBS online sports venue reservation system v1.0 - File Inclusion

### You do not need to log in and open the website storage directory

Supplier:https://www.sourcecodester.com/php/15236/online-sports-complex-booking-system-phpmysql-free-source-code.html

/?p=   ----->    'p' can control some p parameters

Payload:?p=admin/phpinfo

![4](/img/4.png)

We create phpinfo.php under the admin path PHP file, whose content is "<? PHP phpinfo();? >"

![5](/img/5.png)

And visit http://localhost/scbs/?p=admin/phpinfo You can see that phpinfo has been successfully included

![6](/img/6.png)

