# 25個有用的IPtable防火牆規則
```
https://www.howtoing.com/linux-iptables-firewall-rules-examples-commands
```

```
3.阻止IPtables防火牆中的特定IP地址
如果您發現來自IP位址的異常或濫用行為，您可以使用以下規則阻止該IP地址：

# iptables -A INPUT -s xxx.xxx.xxx.xxx -j DROP

```
