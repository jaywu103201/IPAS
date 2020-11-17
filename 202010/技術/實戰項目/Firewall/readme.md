# 實測:
```
使用 iptables 防禦 syn flood 攻擊


```

# 學習目標
```


```

# 系統環境

![FIREWALL.jpg](FIREWALL.jpg)

# 測試步驟
```
1.確認ip
   ifconfig
   ip -4 a
  
2.ping 靶機

   ping -c4   靶機IP

3.使用tcpdump記錄封包
  tcpdump


```
### SYN Flood(洪水) 攻擊
```
原理:

攻擊測試指令:

hping3 -S -p 80 --flood 10.0.2.6

```
### 防火牆規則
```
        iptables -N SYNFLOOD
        iptables -A SYNFLOOD -p tcp --syn -m limit --limit 50/s -j RETURN
        iptables -A SYNFLOOD -p tcp -j LOG --log-level alert
        iptables -A SYNFLOOD -p tcp -j REJECT --reject-with tcp-reset
        iptables -A INPUT -p tcp -m state --state NEW -j SYNFLOOD
```

### tcpdump
```
tcpdump 可用來擷取通過某網路介面的封包

https://blog.xuite.net/jyoutw/xtech/23669726-tcpdump+%E7%9A%84%E7%94%A8%E6%B3%95


基本選項有：
．-n：以數字顯示，不對 IP 作反解，但仍顯示服務名稱。
．-nn：直接以 IP 及 port number 顯示，而非主機名與服務名稱。
．-p：不要以 promiscuous mode 執行。
．-t：不要顯示 timestamp。
．-i：指令要監控的網路介面，如 eth0、lo、any 等。
．-e：使用資料連接層 (OSI 第二層) 的 MAC 封包資料來顯示。
．-c：監聽的封包數，如果沒有這個參數，tcpdump 會持續不斷的監聽，直到使用者輸入 [ctrl]-c 為止。
．-q：僅列出較為簡短的封包資訊，每一行的內容比較精簡。
．-s：抓比較長的 data 做一筆記錄。
．-v：輸出一個稍微詳細的資訊，例如在 IP 封包中可以包括 ttl 和服務類型的資訊。
．-A：封包的內容以 ASCII 顯示，通常用來捉取 WWW 的網頁封包資料。
．-X：可以列出十六進位 (hex) 以及 ASCII 的封包內容，對於監聽封包內容很有用。
．-w：如果你要將監聽所得的封包資料儲存下來，用這個參數就對了！後面接檔名。
．-r：從後面接的檔案將封包資料讀出來。那個『檔案』是已經存在的檔案，並且這個『檔案』是由 -w 所製作出來的。
《範例》 tcpdump -nn -i eth0
```
```
https://www.cnblogs.com/renxinyuan/p/4252019.html
https://kknews.cc/zh-tw/code/oegk9lo.html
```
