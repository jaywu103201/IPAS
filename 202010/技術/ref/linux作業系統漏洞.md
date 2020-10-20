# linux作業系統漏洞
```
linux rootkit
Linux版SMB遠程代碼執行漏洞(CVE-2017-7494)-SambaCry 
```

## linux rootkit
```
挖礦惡意程式攻擊 Linux 系統,並利用 Rootkit 自我隱藏
2018 年 11 月 19 日
挖礦( coinmining )惡意程式
https://blog.trendmicro.com.tw/?p=57986
```
```
Rootkit是一組計算機軟體的合集，通常是惡意的，
它的目的是在非授權的情況下維持系統最高權限（在Unix、Linux下為root，在Windows下為Administrator）來訪問計算機。
與病毒或者木馬不同的是，Rootkit試圖通過隱藏自己來防止被發現，以到達長期利用受害主機的目的。
Rootkit和病毒或者木馬一樣，都會對Linux系統安全產生極大的威脅。

原文網址：https://kknews.cc/code/2y2x4je.html
```
```
Linux Rootkit 研究
https://github.com/NoviceLive/research-rootkit/blob/master/README-zh_CN.rst
```
```
Linux Rootkit
A simple Linux kernel rootkit written for fun, not evil.
https://github.com/nurupo/rootkit
```
```
Kernel-level root kit to test in Docker
https://github.com/ilee38/root-of-all-evil
```
### Linux rootkit的檢測
```
 Linux rootkit的檢測工具使用(chkrootkit和rootkit hunter)
```
```
Linux rootkit的檢測工具使用(chkrootkit和rootkit hunter)
https://www.itread01.com/p/1380252.html

http://linux.vbird.org/linux_security/0420rkhunter.php

https://www.tecmint.com/install-rootkit-hunter-scan-for-rootkits-backdoors-in-linux/
```

### rootkit hunter
```
The Rootkit Hunter project
http://rkhunter.sourceforge.net/
```

```
RootKit Hunter監測木馬和後門偵測
https://ithelp.ithome.com.tw/articles/10161775


安裝指令：sudo apt-get install rkhunter

啟動rkhunter檢查電腦   sudo rkhunter -c

更新資料庫檔案  sudo rkhunter --update

檢查是否有新版本  sudo rkhunter --versioncheck

更新病毒資料庫 sudo rkhunter --propupd
```


```
日誌檔案預設存放在 /var/log/rkhunter.log

https://it001.pixnet.net/blog/post/330454531
```

### Rootkit 分析
```
Forensic analysis of a Rootkit with Sysdig Inspect
觀看次數：1,310次•2017年12月13日
https://www.youtube.com/watch?v=QqNRNhOcpgo
```
## Linux版SMB遠程代碼執行漏洞(CVE-2017-7494)-SambaCry 
```
https://www.itdaan.com/tw/b6fb454e3466
```
```
檢測漏洞是否存在
1） 本地檢查Samba版本是否屬於 4.4.14、 4.5.10、4.6.4 及以后的版本。
2） 使用nmap –script=smb-os-discovery -p 445 192.168.1.122/24    命令掃描網絡中Linux Samba版本。
```

```
How to Fix SambaCry Vulnerability (CVE-2017-7494) in Linux Systems
https://www.tecmint.com/fix-sambacry-vulnerability-cve-2017-7494-in-linux/
```
```
https://www.shodan.io/

查samba
```
##
```

```


##
```

```


##
```

```


##
```

```


##
```

```

