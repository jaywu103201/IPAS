# OWASP TOP 10
```
新版OWASP十大網站安全風險排名出爐，微服務風潮帶來三大新安全風險
OWASP在11月20日公布最新版十大網站資安風險，納入社群建議和實際調查結果後，調整了多項資安風險項目，
各平臺常見的XML外部處理器漏洞，Java平臺、PHP或Node.js等平臺常見的不安全反序列化漏洞，
以及紀錄與監控不足風險，則是2017年上榜的網路安全新風險
文/黃彥棻 | 2017-11-21發表
https://www.ithome.com.tw/news/118411
```

```
https://download.nccst.nat.gov.tw/attachfilehandout/%E8%AD%B0%E9%A1%8C%E4%BA%8C%EF%BC%9A107_OWASP_TOP10_2017.pdf

A1 注入 Injection
A2 身分鑑別相關功能缺陷 Broken Authentication
A3 敏感資料暴露 Sensitive Data Exposure
A4 XML外部實體(XXE) XML External Entity
A5 存取控制相關功能缺陷 Broken Access Control
A6 不當的安全組態設定 Security Misconfiguration
A7 跨站腳本攻擊 (XSS) Cross-Site Scripting
A8 不安全的反序列化 Insecure Deserialization
A9 使用具有已知弱點的元件 Using Components with Known Vulnerabilities
A10 記錄與監控不足 Insufficient Logging & Monitoring
```
```
https://secbuzzer.co/post/116

A1:2017-Injection　注入攻擊
A2:2017-Broken Authentication　無效的身分驗證
A3:2017-Sensitive Data Exposure　機敏資料外洩
A4:2017-XML External Entities (XXE) [NEW]　XML 外部處理器弱點
A5:2017-Broken Access Control [Merged]　無效的存取控管
```
# OWASP API Top 10
```
OWASP (Open Web Application Security Project) 已逐漸被政府與民間機構列入資安參考指標之一。
OWASP 基金會在 2017 年推出了 OWASP Top 10；
2019 年 9 月更推出了針對 API 的 OWASP API Top 10，蒐集了各種 API 的安全漏洞，彙整出 API 的十大安全問題。 
```
```
OWASP API Top 10弱點剖析
https://secbuzzer.co/post/221
https://secbuzzer.co/post/222
https://secbuzzer.co/post/223
```
## Hitcon Zero DAY

## XSS漏洞

```
麥當勞官網遭爆有XSS漏洞，可解密竊取用戶密碼
使用者登入麥當勞網站時，可要求網站記住用戶的密碼，但研究人員發現麥當勞將密碼存於cookie，且可在用戶端解密，
駭客可透過該站另一個XSS漏洞竊取cookie，就能解密取得用戶的密碼。
文/陳曉莉 | 2017-01-18發表
https://www.ithome.com.tw/news/111254
```


# SSRF
```
 SSRF(Server-Side Request Forgery：服務器端請求偽造)
 是一種有攻擊者構造形成有服務器發起請求的一個安全漏洞。
 一般情況下，SSRF攻擊的目標是從外網無法訪問的內部系統。
 
https://github.com/cujanovic/SSRF-Testing
```
```
年度十大網站攻擊技術公布，臺灣滲透測試專家研究獲第一
最近，2017年十大網站駭客攻擊技法正式出爐，經歷三個多月的提名評選，由出身臺灣的資安研究人員所提出的攻擊技術手法，
從37項提名脫穎而出，獲選為年度第一名。

文/羅正漢 | 2018-10-15發表
https://www.ithome.com.tw/news/126410

第一名的網站攻擊技術──SSRF的新時代，是由臺灣的安全研究人員Orange Tsai（蔡政達）所提出
```
```
A New Era of SSRF - Exploiting URL Parser in Trending Programming Languages!
觀看次數：1,277次•2020年1月8日
https://www.youtube.com/watch?v=D1S-G8rJrEk


#HITBGSEC 2017 SG Conf D1 - A New Era Of SSRF - Exploiting Url Parsers - Orange Tsai
https://www.youtube.com/watch?v=D1S-G8rJrEk

CB17] A New Era of SSRF - Exploiting URL Parser in Trending Programming Languages!
觀看次數：6,702次•2017年12月24日
https://www.youtube.com/watch?v=2MslLrPinm0

A New Era of SSRF - Exploiting URL Parser in Trending Programming Languages!
觀看次數：111次•2019年1月23日
https://www.youtube.com/watch?v=cl8j7_QtHig
```
