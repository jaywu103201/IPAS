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
## A1 注入 Injection
```
攻擊者在網頁裡任何可以輸入資料的地方試著去猜想設計者背後的語法撰寫方式，
並去猜測完整的command應該會長成怎麼樣，還有推測欄位數，table的名字，SQL的版本資訊，試著去拼湊輸入一條SQL指令，
輕則刪掉資料庫，重則竊取全部的個資。可以說是任何一個撰寫互動式網頁的開發者首先也必要處理的問題。

一些常見的注入，包括：SQL、NoSQL 、 OS命令、ORM、LDAP和運算式語言（EL）或Object Graph Navigation Library (OGNL)注入。
使用者的輸入被拼接到指令、查詢語句中
使用者輸入的資料沒有經過應用程式的驗證、過濾。
注入漏洞可通過原始碼檢測發現
常用漏洞掃描器或模糊測試工具找到這些漏洞
注入攻擊有時甚至能導致主機被完全接管

防範方式：
1.不要使用串接的查詢語法，改為使用參數化的查詢方式 ( 例如 : Prepared statements)
2.錯誤的訊息不應該顯示給管理員以外的人，以防攻擊者得到更多有用的資訊；
3.嚴密檢查使用者輸入的任何字串，檢查檢查再檢查
4.控管使用者的帳號權限；
5.原始碼審查(Source code review)是最有效的檢測應用程式注入風險的辦法之一
6.白名單

常見的攻擊方式：
1.Sqli -> SQL Injection
2.Command injection
3.LDAP injection
4.XPATH injection
```
## A2 身分鑑別相關功能缺陷 Broken Authentication
```
https://secbuzzer.co/post/116

發生的原因：
脆弱的帳戶認證、不安全的管理機制。
例如：登入未加密、Session 無控管 Cookie 為保護等。
這容易造成帳號 / 身分盜用，或身分認證機制無效化，
讓有心人士可肆意在伺服器做任何新增修改刪除查詢，進而接管主機等。

防範方式：
1.使用完善的 Cookie Session 保護機制。
2.不允許外部 Session。
3.登入及修改資訊頁面使用 SSL 加密。
4.設定完善的 Timeout 機制。
5.多因素認證。
6.驗證密碼強度及密碼定期更換機制。
```
## A3 敏感資料暴露 Sensitive Data Exposure
```
主要分為兩個問題，
1.網站在與使用者傳輸敏感資料時未使用SSL加密連線，導致傳輸有可能被攔截竊聽造成使用者的帳密被盜用；
2.資料未加密、或使用脆弱的金鑰時，容易使得密碼被攻破

防範方式：
1.通通使用SSL安全連線來傳輸；
2.密碼必須使用不可逆的演算法加密後再存在資料庫裡，登入時只需比對加密後的結果是否相同。
3.使用對稱式加密
4.使用公開、具國際機構驗證且未遭破解的演算法
5.使用最大限度之金鑰長度
```
## A4 XML外部實體(XXE) XML External Entity
```
以 XML 為基礎的網路應用程式沒有做好管控權限，直接讀取外部資源提供的 XML 檔案，
如果攻擊者可以上傳XML檔案或者在XML檔案中添加惡意內容，他們就能夠攻擊含有缺陷的XML處理器，
XXE缺陷可用於提取資料、執行遠端服務器請求、掃描內部系統、執行拒絕服務攻擊和其他攻擊。

防範方式：
1.禁止外部實體引用。
2.修補或升級套件，並將 XML 升級到最新。
```
## A5 存取控制相關功能缺陷 Broken Access Control
```
存取控制強制實施策略，使用戶無法在其預期的許可權之外執行行為。
失敗的存取控制通常導致未經授權的資訊洩露、修改或銷毀所有資料、或在使用者許可權之外執行業務功能;
系統服務有存取控制漏洞導致駭客可以進行未授權的行為

防範方式：
1.請求參數必須在伺服器端進行驗證
```
## A6 不當的安全組態設定 Security Misconfiguration
```
1.未刪除或更改所使用的預設帳密及相關預設資料，攻擊者可輕易的透過官方預設的資料嘗試非法入侵
3.錯誤訊息直接顯示在客戶端頁面上，透露太多不必要的額外資訊給攻擊者；
4.未刪除預設範例程式

防範方式：
1.更改所有預設port、頁面、帳號密碼等
2.功能最小化關閉、刪除不必要的功能，刪除所有未使用範例程式、頁面、功能等
```
## A7 跨站腳本攻擊 (XSS) Cross-Site Scripting
```
Crossing Site Scripting (XSS)
網站缺乏適當的驗證，使得攻擊者能網站漏洞把惡意的腳本代碼注入到網頁中，
讓受害者(客戶端)執行惡意程式/指令(JavaScript)，
甚至是將使用者轉址至惡意網站，
自動化工具能自動發現一些XSS問題，
特別是在一些成熟的技術中，如：PHP、J2EE或JSP、ASP.NET

自動化攻擊工具：XSSER、XSSSNIPER、XSSploit

跨站腳本攻擊分為以下三種：

1.反射式(Reflected XSS)：
- 網頁直接將未經驗證的輸入作為HTML 解析並輸出，可讓受害者的瀏覽器中執行任意的HTML和JavaScript。

2.儲存型(Stored XSS)：
- 網頁直接將未經驗證的輸入儲存於伺服器中，可讓訪問者執行任意的HTML和JavaScript，常見於留言板等功能。

3.基於DOM的XSS(DOM XSS)：
- 會動態的將攻擊者可控的內容加入頁面的JavaScript框架、單頁面程式或API存在這種類型的漏洞。

防範方式：
1.資料驗證 (data validation)：對用戶的輸入進行適當的過濾與處理
2.不管是使用者輸入還是頁面輸出都應該要有檢查的機制；
3.可以使用白名單機制；
4.過濾掉有問題的字串(例如PHP可以使用htmlentities)
5.使用安全的瀏覽器：Chrome、Firefox... ...
```
## A8 不安全的反序列化 Insecure Deserialization
```
https://secbuzzer.co/post/115
https://ithelp.ithome.com.tw/articles/10250483?sc=hot

當攻擊者提供竄改後的惡意物件進行反序列化，可能導致應用程式或 API 出現不安全的風險，
例如：注入攻擊（Injection）、跨站腳本攻擊（XSS）、遠端程式碼執行。

序列化就是把物件轉成可儲存化的格式，如json
反序列化就是把儲存格是轉換成物件

防範方式：
1.不接受來自不信任來源的序列化物件。
2.只允許原始資料型態進行反序列化。
3.將序列化的物件加上數位簽章或進行加密，防止新增惡意物件或資料竄改。
4.記錄反序列化所發生的例外情況與失敗訊息。
5.監控反序列化，當用戶持續進行反序列化時，應啟動警告機制。
```
## A9 使用具有已知弱點的元件 Using Components with Known Vulnerabilities
```
https://www.ithome.com.tw/news/131912
名為ruri12的用戶在2017年11月，於PyPI上發布了3個有問題的套件，分別為libpeshnx、libpesh以及libari

使用的元件未更新到最新版本，且該元件已有弱點存在，攻擊者可能對此弱點進行攻擊

雖然對於一些已知的漏洞其影響很小，但目前很多嚴重的安全事件都是利用元件中的已知漏洞。


防範方式：
1.針對已使用的套件定期做版本更新
2.刪除未使用的項目，不必要的功能、組件、檔案…
3.針對已使用的套件定期在 CVE、Exploit DB 或 NVD 做漏洞檢核
4.追蹤相關最新資安訊息
5.定期做弱點掃描：WebInspect、Acunetix
```
## A10 記錄與監控不足 Insufficient Logging & Monitoring
```
1.未記錄可稽核性事件，如：登入、登入失敗和高額交易
2.告警和錯誤事件未能產生或產生不足的和不清晰的日誌資訊。
3.沒有利用應用系統和API的日誌資訊來監控可疑活動。
4.日誌資訊僅在本機存放區。
等等

https://secbuzzer.co/post/115
防範方式：
1.確保登錄、存取失敗、驗證失敗的訊息都能被完整記錄，並保留足夠的用戶資訊，以辨別可疑或惡意行為。
2.確保高額交易能有完整的審計訊息（audit trail），以防被竄改或刪除。
3.建立有效的監控與警告機制，使可疑活動在短時間內能夠被發現及應對。
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
```
https://www.gss.com.tw/focus/security/2285-gss-0173-APISecurity-owasp-checkmarx

API1：2019－Broken Object Level Authorization(不安全的物件授權)
API2：2019－Broken Authentication(無效身分認證)
API3：2019－Excessive Data Exposure(資料暴露不當)
API4：2019－Lack of Resources & Rate Limiting(缺乏資源與速率限制)
API5：2019－Broken Function Level Authorization(無效功能權限控管)
```
## API1：2019－Broken Object Level Authorization(不安全的物件授權)
```
未經過授權，可以任意存取其他ID身分的資料，
非授權的帳號能存取甚至修改到他人帳號的資料，
攻擊者可以透過客戶端發送的請求(目標ID)，進而利用不安全授權的API

防範方式：
1.在進行相關 API 參數進行請求時，增加使用者的授權驗證
2.使用隨機且不可預測的值當作 ID
3.確認是否登入的使用者有權使用其要求的動作
```
## API2：2019－Broken Authentication(無效身分認證)
```
攻擊者可能會透過使用說明手冊來確認無效的身份驗證，
但通常都會留意密碼轉儲、字典攻擊等攻擊，
或者在類似於釣魚或社會工程攻擊之後，發現失效的身份認證

防範方式：
1.使用多重因素認證(Multi-Factor Authentication)
2.避免使用弱密碼
3.API金鑰不應使用在使用者身分認證，僅適用於授權機制
```
## API3：2019－Excessive Data Exposure(資料暴露不當)
```
API端點經常會暴露機敏資訊，攻擊者會用此資訊來尋找不應公開的敏感資料

防範方式：
1.於伺服器端過濾資料後再回傳給使用者
2.不使用 Client 端做敏感資料的過濾及分析
3.明確定義回傳的資料內容
```
## API4：2019－Lack of Resources & Rate Limiting(缺乏資源與速率限制)
```
沒有做好資源大小或速率存取限制，通過大量連線的方式也容易遭受 DDoS 攻擊

防範方式：
1.設定 Client 能再次呼叫 API 的時間限制
2.增加伺服器驗證，控制回應數量參數
```
## API5：2019－Broken Function Level Authorization(無效功能權限控管)
```
攻擊者能透過合法 API 來取得未經授權的資料，
並且越有結構、架構性的資料越好取得，
因為可以透過簡單的預測，去修改 API 路徑與其值

防範方式：
1.拒絕在預設的情況下接受所有來自Client端的存取
2.明確制定使用者帳戶可以訪問、訪問、存取的功能項目
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

https://websec.readthedocs.io/zh/latest/vuln/ssrf.html
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
