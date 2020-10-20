# windows作業系統漏洞
```
MS08-067 
MS17-010 
CVE-2020-0796
WannaCry
```
## MS08-067 
```
https://docs.microsoft.com/zh-tw/security-updates/securitybulletins/2008/ms08-067
```
###  MS08-067漏洞原理分析及還原
```
https://zhuanlan.zhihu.com/p/27155431
```
### 
### 
### MS17-010 

### CVE-2020-0796
```
微軟緊急修補SMB蠕蟲漏洞
微軟一項沒有準時在本月Patch Tuesday發布修補，導致名聲已經傳遍資安圈的Server Message Block（SMB）重大漏洞，在遲到二天後終於補上
文/陳曉莉 | 2020-03-13發表

https://www.ithome.com.tw/news/136330
```
```
CVE-2020-0796：SMB通信協議新漏洞

攻擊者可以利用此漏洞在SMB服務器或SMB客戶端上執行任意代碼。攻擊者只要發送精心構造的數據包就能攻擊服務器。
而要想攻擊客戶端，攻擊者則須先配置一個惡意的SMBv3服務器，並讓用戶連接到它。

網路安全專家認為，該漏洞可被用於啟動類似WannaCry的蠕蟲病毒。微軟表示該漏洞非常嚴重，必須盡快關閉。

https://www.kaspersky-member.com.tw/blog/2020/03/24/cve-2020-0796%EF%BC%9Asmb%E9%80%9A%E4%BF%A1%E5%8D%94%E8%AD%B0%E6%96%B0%E6%BC%8F%E6%B4%9E-2/

SMB服務器：
通過PowerShell 指令阻止該漏洞被利用：
Set-ItemProperty -Path “HKLM:\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters” DisableCompression -Type DWORD -Value 1 –Force
```
```
Windows SMB Ghost（CVE-2020-0796）漏洞分析
發表於 2020-04-10

https://iter01.com/500227.html
```

# 史上第一勒索蠕蟲WannaCry
```
https://www.ithome.com.tw/foucs/114242
```

```

```
